# AWS Lambda Function TracingConfig<a name="aws-properties-lambda-function-tracingconfig"></a>

`TracingConfig` is a property of the [AWS::Lambda::Function](aws-resource-lambda-function.md) resource that configures tracing settings for your AWS Lambda \(Lambda\) function\. For more information about tracing Lambda functions, see [Tracing Lambda\-Based Applications with AWS X\-Ray](http://docs.aws.amazon.com/lambda/latest/dg/lambda-x-ray.html#using-x-ray) in the *AWS Lambda Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1533b5"></a>

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

## Properties<a name="w3ab2c21c14e1533b7"></a>

`Mode`  <a name="cfn-lambda-function-tracingconfig-mode"></a>
Specifies how Lambda traces a request\. The default mode is `PassThrough`\. For more information, see [http://docs.aws.amazon.com/lambda/latest/dg/API_TracingConfig.html](http://docs.aws.amazon.com/lambda/latest/dg/API_TracingConfig.html) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)