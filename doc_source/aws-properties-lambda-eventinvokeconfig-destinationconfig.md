# AWS::Lambda::EventInvokeConfig DestinationConfig<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig"></a>

A configuration object that specifies the destination of an event after Lambda processes it\.

## Syntax<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-syntax.json"></a>

```
{
  "[OnFailure](#cfn-lambda-eventinvokeconfig-destinationconfig-onfailure)" : OnFailure,
  "[OnSuccess](#cfn-lambda-eventinvokeconfig-destinationconfig-onsuccess)" : OnSuccess
}
```

### YAML<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-syntax.yaml"></a>

```
  [OnFailure](#cfn-lambda-eventinvokeconfig-destinationconfig-onfailure): 
    OnFailure
  [OnSuccess](#cfn-lambda-eventinvokeconfig-destinationconfig-onsuccess): 
    OnSuccess
```

## Properties<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-properties"></a>

`OnFailure`  <a name="cfn-lambda-eventinvokeconfig-destinationconfig-onfailure"></a>
The destination configuration for failed invocations\.  
*Required*: No  
*Type*: [OnFailure](aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnSuccess`  <a name="cfn-lambda-eventinvokeconfig-destinationconfig-onsuccess"></a>
The destination configuration for successful invocations\.  
*Required*: No  
*Type*: [OnSuccess](aws-properties-lambda-eventinvokeconfig-destinationconfig-onsuccess.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig--examples"></a>



### On\-Failure Destination Configuration<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig--examples--On-Failure_Destination_Configuration"></a>

Configure a function to send a record of failed asynchronous invocations to an SQS queue\.

#### YAML<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig--examples--On-Failure_Destination_Configuration--yaml"></a>

```
      DestinationConfig:
          OnFailure:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
```