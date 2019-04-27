# AWS::Lambda::Function<a name="aws-resource-lambda-function"></a>

The `AWS::Lambda::Function` resource creates an AWS Lambda \(Lambda\) function that can run code in response to events\. To create a function, you need a [deployment package](https://docs.aws.amazon.com/lambda/latest/dg/deployment-package-v2.html) and an [execution role](https://docs.aws.amazon.com/lambda/latest/dg/intro-permission-model.html#lambda-intro-execution-role)\. For more information, see `[CreateFunction](https://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html)` in the *AWS Lambda Developer Guide*\.

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
    "[Layers](#cfn-lambda-function-layers)" : [ String, ... ],
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
  [Layers](#cfn-lambda-function-layers): 
    - String
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

## Properties<a name="w2922ab1c21c10d166c21b7"></a>

For more information about each property, including defaults, valid values, and constraints, see [CreateFunction](https://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html) in the *AWS Lambda Developer Guide*\.

`Code`  <a name="cfn-lambda-function-code"></a>
The code for the function\.  
*Required*: Yes  
*Type*: [AWS Lambda Function Code](aws-properties-lambda-function-code.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-lambda-function-deadletterconfig"></a>
A dead letter queue configuration that specifies the queue or topic where Lambda sends asynchronous events when they fail processing\. For more information, see [Dead Letter Queues](https://docs.aws.amazon.com/lambda/latest/dg/dlq.html)\.  
*Required*: No  
*Type*: [AWS Lambda Function DeadLetterConfig](aws-properties-lambda-function-deadletterconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-lambda-function-description"></a>
A description of the function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Environment`  <a name="cfn-lambda-function-environment"></a>
Environment variables that are accessible from function code during execution\.  
*Required*: No  
*Type*: [AWS Lambda Function Environment](aws-properties-lambda-function-environment.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-function-functionname"></a>
The name of the Lambda function\. If you don't specify a name, AWS CloudFormation generates one\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Handler`  <a name="cfn-lambda-function-handler"></a>
The name of the method within your code that Lambda calls to execute your function\. The format includes the filename and can also include namespaces and other qualifiers, depending on the runtime\. For more information, see [Programming Model](https://docs.aws.amazon.com/lambda/latest/dg/programming-model-v2.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-lambda-function-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service key used to encrypt your function's environment variables\. If not provided, Lambda uses a default service key\.  
*Type*: String  
*Required*: No  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Layers`  <a name="cfn-lambda-function-layers"></a>
A list of [function layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) to add to the function's execution environment\. Specify each layer by ARN, including the version\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MemorySize`  <a name="cfn-lambda-function-memorysize"></a>
The amount of memory that your function has access to\. Increasing the function's memory also increases it's CPU allocation\. The default value is 128 MB\. The value must be a multiple of 64 MB\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReservedConcurrentExecutions`  <a name="cfn-lambda-function-reservedconcurrentexecutions"></a>
The maximum number of instances of your function that process events simultaneously\. This option both sets the maximum concurrency for your function and reserves concurrency to ensure that it is available\. For more information, see [Managing Concurrency](https://docs.aws.amazon.com/lambda/latest/dg/concurrent-executions.html) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Role`  <a name="cfn-lambda-function-role"></a>
The ARN of the function's execution role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Runtime`  <a name="cfn-lambda-function-runtime"></a>
The identifier of the function's [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Timeout`  <a name="cfn-lambda-function-timeout"></a>
The amount of time that Lambda allows a function to run before terminating it\. The default is 3 seconds\. The maximum allowed value is 900 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TracingConfig`  <a name="cfn-lambda-function-tracingconfig"></a>
Set `Mode` to `Active` to sample and trace a subset of incoming requests with AWS X\-Ray\.  
*Required*: No  
*Type*: [AWS Lambda Function TracingConfig](aws-properties-lambda-function-tracingconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcConfig`  <a name="cfn-lambda-function-vpcconfig"></a>
For network connectivity to AWS resources in a VPC, specify a list of security groups and subnets in the VPC\. When you connect a function to a VPC, it can only access resources and the internet through that VPC\. For more information, see [VPC Settings](https://docs.aws.amazon.com/lambda/latest/dg/vpc.html)\.  
When you specify this property, AWS CloudFormation might not be able to delete the stack if another resource in the template \(such as a security group\) requires the attached ENI to be deleted before it can be deleted\. We recommend that you run AWS CloudFormation with the `ec2:DescribeNetworkInterfaces` permission, which enables AWS CloudFormation to monitor the state of the ENI and to wait \(up to 40 minutes\) for Lambda to delete the ENI\.
*Required*: No  
*Type*: [AWS Lambda Function VpcConfig](aws-properties-lambda-function-vpcconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-lambda-function-tags"></a>
A list of [tags](https://docs.aws.amazon.com/lambda/latest/dg/tagging.html) to apply to the function\.  
*Required*: No  
*Type*: [Resource Tag](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w2922ab1c21c10d166c21b9"></a>

### Ref<a name="w2922ab1c21c10d166c21b9b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

In the following sample, the `Ref` function returns the name of the `AMILookUp` function, such as `MyStack-AMILookUp-NT5EUXTNTXXD`\.

```
{ "Ref": "AMILookUp" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w2922ab1c21c10d166c21b9b5"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The ARN of the Lambda function, such as `arn:aws:lambda:us-west-2:123456789012:MyStack-AMILookUp-NT5EUXTNTXXD`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w2922ab1c21c10d166c21c11"></a>

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
    "Runtime": "nodejs8.10",
    "Timeout": 25,
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
    Runtime: "nodejs8.10"
    Timeout: 25
    TracingConfig:
      Mode: "Active"
```

## Related Resources<a name="w2922ab1c21c10d166c21c13"></a>

For more information about how you can use a Lambda function with AWS CloudFormation custom resources, see [AWS Lambda\-backed Custom Resources](template-custom-resources-lambda.md)\.

For a sample template, see [AWS Lambda Template](quickref-lambda.md)\.