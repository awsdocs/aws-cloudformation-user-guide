# AWS::Lambda::Function<a name="aws-resource-lambda-function"></a>

The `AWS::Lambda::Function` resource creates an AWS Lambda \(Lambda\) function that can run code in response to events\. For more information, see `[CreateFunction](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html)` in the *AWS Lambda Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-lambda-function-syntax)
+ [Properties](#w3ab2c21c10d855b9)
+ [Return Values](#w3ab2c21c10d855c11)
+ [Example](#w3ab2c21c10d855c13)
+ [Related Resources](#w3ab2c21c10d855c15)

## Syntax<a name="aws-resource-lambda-function-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-function-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Function",
  "Properties" : {
    "[Code](#cfn-lambda-function-code)" : Code,
    "[DeadLetterConfig](#cfn-lambda-function-deadletterconfig)" : [*DeadLetterConfig*](aws-properties-lambda-function-deadletterconfig.md),
    "[Description](#cfn-lambda-function-description)" : String,
    "[Environment](#cfn-lambda-function-environment)" : [*Environment*](aws-properties-lambda-function-environment.md),
    "[FunctionName](#cfn-lambda-function-functionname)" : String,
    "[Handler](#cfn-lambda-function-handler)" : String,
    "[KmsKeyArn](#cfn-lambda-function-kmskeyarn)" : String,
    "[MemorySize](#cfn-lambda-function-memorysize)" : Integer,
    "[ReservedConcurrentExecutions](#cfn-lambda-function-reservedconcurrentexecutions)" : Integer,
    "[Role](#cfn-lambda-function-role)" : String,
    "[Runtime](#cfn-lambda-function-runtime)" : String,
    "[Timeout](#cfn-lambda-function-timeout)" : Integer,
    "[TracingConfig](#cfn-lambda-function-tracingconfig)" : [*TracingConfig*](aws-properties-lambda-function-tracingconfig.md),
    "[VpcConfig](#cfn-lambda-function-vpcconfig)" : [*VPCConfig*](aws-properties-lambda-function-vpcconfig.md),
    "[Tags](#cfn-lambda-function-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-lambda-function-syntax.yaml"></a>

```
Type: "AWS::Lambda::Function"
Properties: 
  [Code](#cfn-lambda-function-code):
    Code
  [DeadLetterConfig](#cfn-lambda-function-deadletterconfig):
    [*DeadLetterConfig*](aws-properties-lambda-function-deadletterconfig.md)
  [Description](#cfn-lambda-function-description): String
  [Environment](#cfn-lambda-function-environment):
    [*Environment*](aws-properties-lambda-function-environment.md)
  [FunctionName](#cfn-lambda-function-functionname): String
  [Handler](#cfn-lambda-function-handler): String
  [KmsKeyArn](#cfn-lambda-function-kmskeyarn): String
  [MemorySize](#cfn-lambda-function-memorysize): Integer
  [ReservedConcurrentExecutions](#cfn-lambda-function-reservedconcurrentexecutions): Integer
  [Role](#cfn-lambda-function-role): String
  [Runtime](#cfn-lambda-function-runtime): String
  [Timeout](#cfn-lambda-function-timeout): Integer
  [TracingConfig](#cfn-lambda-function-tracingconfig):
    [*TracingConfig*](aws-properties-lambda-function-tracingconfig.md)
  [VpcConfig](#cfn-lambda-function-vpcconfig):
    [*VPCConfig*](aws-properties-lambda-function-vpcconfig.md)
  [Tags](#cfn-lambda-function-tags): 
    Resource Tag
```

## Properties<a name="w3ab2c21c10d855b9"></a>

`Code`  <a name="cfn-lambda-function-code"></a>
The source code of your Lambda function\. You can point to a file in an Amazon Simple Storage Service \(Amazon S3\) bucket or specify your source code as inline text\.  
*Required*: Yes  
*Type*: [AWS Lambda Function Code](aws-properties-lambda-function-code.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-lambda-function-deadletterconfig"></a>
Configures how Lambda handles events that it can't process\. If you don't specify a Dead Letter Queue \(DLQ\) configuration, Lambda discards events after the maximum number of retries\. For more information, see [Dead Letter Queues](http://docs.aws.amazon.com/lambda/latest/dg/dlq.html) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: [AWS Lambda Function DeadLetterConfig](aws-properties-lambda-function-deadletterconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-lambda-function-description"></a>
A description of the function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Environment`  <a name="cfn-lambda-function-environment"></a>
Key\-value pairs that Lambda caches and makes available for your Lambda functions\. Use environment variables to apply configuration changes, such as test and production environment configurations, without changing your Lambda function source code\.  
*Required*: No  
*Type*: [AWS Lambda Function Environment](aws-properties-lambda-function-environment.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-function-functionname"></a>
A name for the function\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the function's name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Handler`  <a name="cfn-lambda-function-handler"></a>
The name of the function \(within your source code\) that Lambda calls to start running your code\. For more information, see the `[Handler](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html#SSS-CreateFunction-request-Handler)` property in the *AWS Lambda Developer Guide*\.  
If you specify your source code as inline text by specifying the `ZipFile` property within the `Code` property, specify `index.function_name` as the handler\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-lambda-function-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Key Management Service \(AWS KMS\) key that Lambda uses to encrypt and decrypt environment variable values\.  
*Type*: String  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MemorySize`  <a name="cfn-lambda-function-memorysize"></a>
The amount of memory, in MB, that is allocated to your Lambda function\. Lambda uses this value to proportionally allocate the amount of CPU power\. For more information, see [Resource Model](http://docs.aws.amazon.com/lambda/latest/dg/resource-model.html) in the *AWS Lambda Developer Guide*\.  

Your function use case determines your CPU and memory requirements\. For example, a database operation might need less memory than an image processing function\. You must specify a value that is greater than or equal to `128`, and it must be a multiple of 64\. You cannot specify a size larger than `3008`\. The default value is 128 MB\.  
*Required: *No
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReservedConcurrentExecutions`  <a name="cfn-lambda-function-reservedconcurrentexecutions"></a>
The maximum of concurrent executions you want reserved for the function\. For more information on reserved concurrency limits, see [Managing Concurrency](http://docs.aws.amazon.com/lambda/latest/dg/concurrent-executions.html) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Role`  <a name="cfn-lambda-function-role"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) execution role that Lambda assumes when it runs your code to access AWS services\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Runtime`  <a name="cfn-lambda-function-runtime"></a>
The runtime environment for the Lambda function that you are uploading\. For valid values, see the [Runtime](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html#SSS-CreateFunction-request-Runtime) property in the *AWS Lambda Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
Because Node\.js 0\.10\.32 has been deprecated, you can no longer roll back a template that uses Node\.js 0\.10\.32\. If you update a stack to Node\.js 0\.10\.32 and the update fails, AWS CloudFormation won't roll it back\.

`Timeout`  <a name="cfn-lambda-function-timeout"></a>
The function execution time \(in seconds\) after which Lambda terminates the function\. Because the execution time affects cost, set this value based on the function's expected execution time\. By default, `Timeout` is set to `3` seconds\. For more information, see the [FAQs](https://aws.amazon.com//lambda/faqs/)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TracingConfig`  <a name="cfn-lambda-function-tracingconfig"></a>
The parent object that contains your Lambda function's tracing settings\. By default, the `Mode` property is set to `PassThrough`\. For valid values, see the [TracingConfig](http://docs.aws.amazon.com/lambda/latest/dg/API_TracingConfig.html) data type in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: [AWS Lambda Function TracingConfig](aws-properties-lambda-function-tracingconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcConfig`  <a name="cfn-lambda-function-vpcconfig"></a>
If the Lambda function requires access to resources in a VPC, specify a VPC configuration that Lambda uses to set up an elastic network interface \(ENI\)\. The ENI enables your function to connect to other resources in your VPC, but it doesn't provide public Internet access\. If your function requires Internet access \(for example, to access AWS services that don't have VPC endpoints\), configure a Network Address Translation \(NAT\) instance inside your VPC or use an Amazon Virtual Private Cloud \(Amazon VPC\) NAT gateway\. For more information, see [NAT Gateways](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-nat-gateway.html) in the *Amazon VPC User Guide*\.  
When you specify this property, AWS CloudFormation might not be able to delete the stack if another resource in the template \(such as a security group\) requires the attached ENI to be deleted before it can be deleted\. We recommend that you run AWS CloudFormation with the `ec2:DescribeNetworkInterfaces` permission, which enables AWS CloudFormation to monitor the state of the ENI and to wait \(up to 40 minutes\) for Lambda to delete the ENI\.
*Required*: No  
*Type*: [AWS Lambda Function VpcConfig](aws-properties-lambda-function-vpcconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-lambda-function-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this Lambda function\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d855c11"></a>

### Ref<a name="w3ab2c21c10d855c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

In the following sample, the `Ref` function returns the name of the `AMILookUp` function, such as `MyStack-AMILookUp-NT5EUXTNTXXD`\.

```
{ "Ref": "AMILookUp" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d855c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The ARN of the Lambda function, such as `arn:aws:lambda:us-west-2:123456789012:MyStack-AMILookUp-NT5EUXTNTXXD`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d855c13"></a>

The following example uses a packaged file in an S3 bucket to create a Lambda function\.

### JSON<a name="aws-resource-lambda-function-example.json"></a>

```
"AMIIDLookup": {
  "Type": "AWS::Lambda::Function",
  "Properties": {
    "Handler": "index.handler",
    "Role": { "Fn::GetAtt" : ["LambdaExecutionRole", "Arn"] },
    "Code": {
      "S3Bucket": "lambda-functions",
      "S3Key": "amilookup.zip"
    },
    "Runtime": "nodejs4.3",
    "Timeout": "25",
    "TracingConfig": {
      "Mode": "Active"
   }
  }
}
```

### YAML<a name="aws-resource-lambda-function-example.yaml"></a>

```
AMIIDLookup: 
  Type: "AWS::Lambda::Function"
  Properties: 
    Handler: "index.handler"
    Role: 
      Fn::GetAtt: 
        - "LambdaExecutionRole"
        - "Arn"
    Code: 
      S3Bucket: "lambda-functions"
      S3Key: "amilookup.zip"
    Runtime: "nodejs4.3"
    Timeout: "25"
    TracingConfig:
      Mode: "Active"
```

## Related Resources<a name="w3ab2c21c10d855c15"></a>

For more information about how you can use a Lambda function with AWS CloudFormation custom resources, see [AWS Lambda\-backed Custom Resources](template-custom-resources-lambda.md)\.

For a sample template, see [AWS Lambda Template](quickref-lambda.md)\.
