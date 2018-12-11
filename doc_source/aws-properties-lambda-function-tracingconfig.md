# AWS Lambda Function TracingConfig<a name="aws-properties-lambda-function-tracingconfig"></a>

`TracingConfig` is a property of the [AWS::Lambda::Function](aws-resource-lambda-function.md) resource that configures tracing settings for your AWS Lambda \(Lambda\) function\. For more information about tracing Lambda functions, see [Tracing Lambda\-Based Applications with AWS X\-Ray](https://docs.aws.amazon.com/lambda/latest/dg/lambda-x-ray.html#using-x-ray) in the *AWS Lambda Developer Guide*\.

## Syntax<a name="w4ab1c21c10d162c21c30b5"></a>

### JSON<a name="aws-properties-lambda-function-tracingconfig-syntax.json"></a>

```
{
  "[Mode](#cfn-lambda-function-tracingconfig-mode)" : String
}
```

### YAML<a name="aws-properties-lambda-function-tracingconfig-syntax.yaml"></a>

```
[Mode](#cfn-lambda-function-tracingconfig-mode):
  String
```

## Properties<a name="w4ab1c21c10d162c21c30b7"></a>

`Mode`  <a name="cfn-lambda-function-tracingconfig-mode"></a>
Specifies how Lambda traces a request\. The default mode is `PassThrough`\. For more information, see [https://docs.aws.amazon.com/lambda/latest/dg/API_TracingConfig.html](https://docs.aws.amazon.com/lambda/latest/dg/API_TracingConfig.html) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)