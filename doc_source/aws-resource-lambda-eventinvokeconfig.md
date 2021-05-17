# AWS::Lambda::EventInvokeConfig<a name="aws-resource-lambda-eventinvokeconfig"></a>

The `AWS::Lambda::EventInvokeConfig` resource configures options for [asynchronous invocation](https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html) on a version or an alias\.

By default, Lambda retries an asynchronous invocation twice if the function returns an error\. It retains events in a queue for up to six hours\. When an event fails all processing attempts or stays in the asynchronous invocation queue for too long, Lambda discards it\.

## Syntax<a name="aws-resource-lambda-eventinvokeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-eventinvokeconfig-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::EventInvokeConfig",
  "Properties" : {
      "[DestinationConfig](#cfn-lambda-eventinvokeconfig-destinationconfig)" : DestinationConfig,
      "[FunctionName](#cfn-lambda-eventinvokeconfig-functionname)" : String,
      "[MaximumEventAgeInSeconds](#cfn-lambda-eventinvokeconfig-maximumeventageinseconds)" : Integer,
      "[MaximumRetryAttempts](#cfn-lambda-eventinvokeconfig-maximumretryattempts)" : Integer,
      "[Qualifier](#cfn-lambda-eventinvokeconfig-qualifier)" : String
    }
}
```

### YAML<a name="aws-resource-lambda-eventinvokeconfig-syntax.yaml"></a>

```
Type: AWS::Lambda::EventInvokeConfig
Properties: 
  [DestinationConfig](#cfn-lambda-eventinvokeconfig-destinationconfig): 
    DestinationConfig
  [FunctionName](#cfn-lambda-eventinvokeconfig-functionname): String
  [MaximumEventAgeInSeconds](#cfn-lambda-eventinvokeconfig-maximumeventageinseconds): Integer
  [MaximumRetryAttempts](#cfn-lambda-eventinvokeconfig-maximumretryattempts): Integer
  [Qualifier](#cfn-lambda-eventinvokeconfig-qualifier): String
```

## Properties<a name="aws-resource-lambda-eventinvokeconfig-properties"></a>

`DestinationConfig`  <a name="cfn-lambda-eventinvokeconfig-destinationconfig"></a>
A destination for events after they have been sent to a function for processing\.  

**Destinations**
+  **Function** \- The Amazon Resource Name \(ARN\) of a Lambda function\.
+  **Queue** \- The ARN of an SQS queue\.
+  **Topic** \- The ARN of an SNS topic\.
+  **Event Bus** \- The ARN of an Amazon EventBridge event bus\.
*Required*: No  
*Type*: [DestinationConfig](aws-properties-lambda-eventinvokeconfig-destinationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-eventinvokeconfig-functionname"></a>
The name of the Lambda function\.  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `([a-zA-Z0-9-_]+)`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaximumEventAgeInSeconds`  <a name="cfn-lambda-eventinvokeconfig-maximumeventageinseconds"></a>
The maximum age of a request that Lambda sends to a function for processing\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `21600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRetryAttempts`  <a name="cfn-lambda-eventinvokeconfig-maximumretryattempts"></a>
The maximum number of times to retry when the function returns an error\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Qualifier`  <a name="cfn-lambda-eventinvokeconfig-qualifier"></a>
The identifier of a version or alias\.  
+ **Version** \- A version number\.
+ **Alias** \- An alias name\.
+ **Latest** \- To specify the unpublished version, use `$LATEST`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `(|[a-zA-Z0-9$_-]+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lambda-eventinvokeconfig-return-values"></a>

### Ref<a name="aws-resource-lambda-eventinvokeconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

## Examples<a name="aws-resource-lambda-eventinvokeconfig--examples"></a>



### Asynchronous Invocation Configuration<a name="aws-resource-lambda-eventinvokeconfig--examples--Asynchronous_Invocation_Configuration"></a>

Error handling and destination configuration for a version of a function\. Node\.js function and version are included\.

#### YAML<a name="aws-resource-lambda-eventinvokeconfig--examples--Asynchronous_Invocation_Configuration--yaml"></a>

```
Resources:
  function:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: arn:aws:iam::123456789012:role/lambda-role
      Code:
        ZipFile: |
          exports.handler = async (event) => {
              console.log(JSON.stringify(event, null, 2));
              const response = {
                  statusCode: 200,
                  body: JSON.stringify('Hello from Lambda!'),
              };
              return response;
          };
      Runtime: nodejs12.x
      TracingConfig:
        Mode: Active
  version:
    Type: AWS::Lambda::Version
    Properties:
      FunctionName: !Ref function
  asyncconfig:
    Type: AWS::Lambda::EventInvokeConfig
    Properties:
      DestinationConfig:
          OnFailure:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
          OnSuccess:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
      FunctionName: !Ref function
      MaximumEventAgeInSeconds: 300
      MaximumRetryAttempts: 1
      Qualifier: !GetAtt version.Version
```