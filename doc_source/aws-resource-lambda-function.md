# AWS::Lambda::Function<a name="aws-resource-lambda-function"></a>

The `AWS::Lambda::Function` resource creates a Lambda function\. To create a function, you need a [deployment package](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html) and an [execution role](https://docs.aws.amazon.com/lambda/latest/dg/lambda-intro-execution-role.html)\. The deployment package contains your function code\. The execution role grants the function permission to use AWS services, such as Amazon CloudWatch Logs for log streaming and AWS X\-Ray for request tracing\.

## Syntax<a name="aws-resource-lambda-function-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-function-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Function",
  "Properties" : {
      "[Code](#cfn-lambda-function-code)" : Code,
      "[CodeSigningConfigArn](#cfn-lambda-function-codesigningconfigarn)" : String,
      "[DeadLetterConfig](#cfn-lambda-function-deadletterconfig)" : DeadLetterConfig,
      "[Description](#cfn-lambda-function-description)" : String,
      "[Environment](#cfn-lambda-function-environment)" : Environment,
      "[FileSystemConfigs](#cfn-lambda-function-filesystemconfigs)" : [ FileSystemConfig, ... ],
      "[FunctionName](#cfn-lambda-function-functionname)" : String,
      "[Handler](#cfn-lambda-function-handler)" : String,
      "[ImageConfig](#cfn-lambda-function-imageconfig)" : ImageConfig,
      "[KmsKeyArn](#cfn-lambda-function-kmskeyarn)" : String,
      "[Layers](#cfn-lambda-function-layers)" : [ String, ... ],
      "[MemorySize](#cfn-lambda-function-memorysize)" : Integer,
      "[PackageType](#cfn-lambda-function-packagetype)" : String,
      "[ReservedConcurrentExecutions](#cfn-lambda-function-reservedconcurrentexecutions)" : Integer,
      "[Role](#cfn-lambda-function-role)" : String,
      "[Runtime](#cfn-lambda-function-runtime)" : String,
      "[Tags](#cfn-lambda-function-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Timeout](#cfn-lambda-function-timeout)" : Integer,
      "[TracingConfig](#cfn-lambda-function-tracingconfig)" : TracingConfig,
      "[VpcConfig](#cfn-lambda-function-vpcconfig)" : VpcConfig
    }
}
```

### YAML<a name="aws-resource-lambda-function-syntax.yaml"></a>

```
Type: AWS::Lambda::Function
Properties: 
  [Code](#cfn-lambda-function-code): 
    Code
  [CodeSigningConfigArn](#cfn-lambda-function-codesigningconfigarn): String
  [DeadLetterConfig](#cfn-lambda-function-deadletterconfig): 
    DeadLetterConfig
  [Description](#cfn-lambda-function-description): String
  [Environment](#cfn-lambda-function-environment): 
    Environment
  [FileSystemConfigs](#cfn-lambda-function-filesystemconfigs): 
    - FileSystemConfig
  [FunctionName](#cfn-lambda-function-functionname): String
  [Handler](#cfn-lambda-function-handler): String
  [ImageConfig](#cfn-lambda-function-imageconfig): 
    ImageConfig
  [KmsKeyArn](#cfn-lambda-function-kmskeyarn): String
  [Layers](#cfn-lambda-function-layers): 
    - String
  [MemorySize](#cfn-lambda-function-memorysize): Integer
  [PackageType](#cfn-lambda-function-packagetype): String
  [ReservedConcurrentExecutions](#cfn-lambda-function-reservedconcurrentexecutions): Integer
  [Role](#cfn-lambda-function-role): String
  [Runtime](#cfn-lambda-function-runtime): String
  [Tags](#cfn-lambda-function-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Timeout](#cfn-lambda-function-timeout): Integer
  [TracingConfig](#cfn-lambda-function-tracingconfig): 
    TracingConfig
  [VpcConfig](#cfn-lambda-function-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-resource-lambda-function-properties"></a>

`Code`  <a name="cfn-lambda-function-code"></a>
The code for the function\.  
*Required*: Yes  
*Type*: [Code](aws-properties-lambda-function-code.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodeSigningConfigArn`  <a name="cfn-lambda-function-codesigningconfigarn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-lambda-function-deadletterconfig"></a>
A dead letter queue configuration that specifies the queue or topic where Lambda sends asynchronous events when they fail processing\. For more information, see [Dead Letter Queues](https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html#dlq)\.  
*Required*: No  
*Type*: [DeadLetterConfig](aws-properties-lambda-function-deadletterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lambda-function-description"></a>
A description of the function\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Environment`  <a name="cfn-lambda-function-environment"></a>
Environment variables that are accessible from function code during execution\.  
*Required*: No  
*Type*: [Environment](aws-properties-lambda-function-environment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemConfigs`  <a name="cfn-lambda-function-filesystemconfigs"></a>
Connection settings for an Amazon EFS file system\. To connect a function to a file system, a mount target must be available in every Availability Zone that your function connects to\. If your template contains an [AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html) resource, you must also specify a `DependsOn` attribute to ensure that the mount target is created or updated before the function\.  
For more information about using the `DependsOn` attribute, see [DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html)\.   
*Required*: No  
*Type*: List of [FileSystemConfig](aws-properties-lambda-function-filesystemconfig.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-function-functionname"></a>
The name of the Lambda function, up to 64 characters in length\. If you don't specify a name, AWS CloudFormation generates one\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Handler`  <a name="cfn-lambda-function-handler"></a>
The name of the method within your code that Lambda calls to execute your function\. The format includes the file name\. It can also include namespaces and other qualifiers, depending on the runtime\. For more information, see [Programming Model](https://docs.aws.amazon.com/lambda/latest/dg/programming-model-v2.html)\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[^\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageConfig`  <a name="cfn-lambda-function-imageconfig"></a>
Configuration values that override the container image Dockerfile settings\. See [Container settings](https://docs.aws.amazon.com/lambda/latest/dg/images-parms.html)\.   
*Required*: No  
*Type*: [ImageConfig](aws-properties-lambda-function-imageconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-lambda-function-kmskeyarn"></a>
The ARN of the AWS Key Management Service \(AWS KMS\) key that's used to encrypt your function's environment variables\. If it's not provided, AWS Lambda uses a default service key\.  
*Required*: No  
*Type*: String  
*Pattern*: `(arn:(aws[a-zA-Z-]*)?:[a-z0-9-.]+:.*)|()`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Layers`  <a name="cfn-lambda-function-layers"></a>
A list of [function layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) to add to the function's execution environment\. Specify each layer by its ARN, including the version\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemorySize`  <a name="cfn-lambda-function-memorysize"></a>
The amount of memory available to the function at runtime\. Increasing the function's memory also increases its CPU allocation\. The default value is 128 MB\. The value can be any multiple of 1 MB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `128`  
*Maximum*: `10240`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PackageType`  <a name="cfn-lambda-function-packagetype"></a>
The type of deployment package\. Set to `Image` for container image and set `Zip` for \.zip file archive\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Image | Zip`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReservedConcurrentExecutions`  <a name="cfn-lambda-function-reservedconcurrentexecutions"></a>
The number of simultaneous executions to reserve for the function\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-lambda-function-role"></a>
The Amazon Resource Name \(ARN\) of the function's execution role\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:(aws[a-zA-Z-]*)?:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Runtime`  <a name="cfn-lambda-function-runtime"></a>
The identifier of the function's [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dotnetcore1.0 | dotnetcore2.0 | dotnetcore2.1 | dotnetcore3.1 | go1.x | java11 | java8 | java8.al2 | nodejs | nodejs10.x | nodejs12.x | nodejs4.3 | nodejs4.3-edge | nodejs6.10 | nodejs8.10 | provided | provided.al2 | python2.7 | python3.6 | python3.7 | python3.8 | ruby2.5 | ruby2.7`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-lambda-function-tags"></a>
A list of [tags](https://docs.aws.amazon.com/lambda/latest/dg/tagging.html) to apply to the function\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-lambda-function-timeout"></a>
The amount of time that Lambda allows a function to run before stopping it\. The default is 3 seconds\. The maximum allowed value is 900 seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TracingConfig`  <a name="cfn-lambda-function-tracingconfig"></a>
Set `Mode` to `Active` to sample and trace a subset of incoming requests with AWS X\-Ray\.  
*Required*: No  
*Type*: [TracingConfig](aws-properties-lambda-function-tracingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-lambda-function-vpcconfig"></a>
For network connectivity to AWS resources in a VPC, specify a list of security groups and subnets in the VPC\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-lambda-function-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lambda-function-return-values"></a>

### Ref<a name="aws-resource-lambda-function-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lambda-function-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lambda-function-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the function\.

## Examples<a name="aws-resource-lambda-function--examples"></a>



### Function<a name="aws-resource-lambda-function--examples--Function"></a>

Create a Node\.js function\.

#### JSON<a name="aws-resource-lambda-function--examples--Function--json"></a>

```
"AMIIDLookup": {
    "Type": "AWS::Lambda::Function",
    "Properties": {
        "Handler": "index.handler",
        "Role": {
            "Fn::GetAtt": [
                "LambdaExecutionRole",
                "Arn"
            ]
        },
        "Code": {
            "S3Bucket": "lambda-functions",
            "S3Key": "amilookup.zip"
        },
        "Runtime": "nodejs12.x",
        "Timeout": 25,
        "TracingConfig": {
            "Mode": "Active"
        }
    }
}
```

### Inline Function<a name="aws-resource-lambda-function--examples--Inline_Function"></a>

Inline Node\.js function that uses the cfn\-response library\.

#### YAML<a name="aws-resource-lambda-function--examples--Inline_Function--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Lambda function with cfn-response.
Resources:
  primer:
    Type: AWS::Lambda::Function
    Properties:
      Runtime: nodejs12.x
      Role: arn:aws:iam::123456789012:role/lambda-role
      Handler: index.handler
      Code:
        ZipFile: |
          var aws = require('aws-sdk')
          var response = require('cfn-response')
          exports.handler = function(event, context) {
              console.log("REQUEST RECEIVED:\n" + JSON.stringify(event))
              // For Delete requests, immediately send a SUCCESS response.
              if (event.RequestType == "Delete") {
                  response.send(event, context, "SUCCESS")
                  return
              }
              var responseStatus = "FAILED"
              var responseData = {}
              var functionName = event.ResourceProperties.FunctionName
              var lambda = new aws.Lambda()
              lambda.invoke({ FunctionName: functionName }, function(err, invokeResult) {
                  if (err) {
                      responseData = {Error: "Invoke call failed"}
                      console.log(responseData.Error + ":\n", err)
                  }
                  else responseStatus = "SUCCESS"
                  response.send(event, context, responseStatus, responseData)
              })
          }
      Description: Invoke a function during stack creation.
      TracingConfig:
        Mode: Active
```

### VPC Function<a name="aws-resource-lambda-function--examples--VPC_Function"></a>

Function connected to a VPC\.

#### YAML<a name="aws-resource-lambda-function--examples--VPC_Function--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: VPC function.
Resources:
  Function:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: arn:aws:iam::123456789012:role/lambda-role
      Code:
        S3Bucket: my-bucket
        S3Key: function.zip
      Runtime: nodejs12.x
      Timeout: 5
      TracingConfig:
        Mode: Active
      VpcConfig:
        SecurityGroupIds:
          - sg-085912345678492fb
        SubnetIds:
          - subnet-071f712345678e7c8
          - subnet-07fd123456788a036
```