# AWS Lambda Function Environment<a name="aws-properties-lambda-function-environment"></a>

`Environment` is a property of the [AWS::Lambda::Function](aws-resource-lambda-function.md) resource that specifies key\-value pairs that the AWS Lambda \(Lambda\) function can access so that you can apply configuration changes, such as test and production environment configurations, without changing the function code\.

## Syntax<a name="w3ab2c21c14e1524b5"></a>

### JSON<a name="aws-properties-lambda-function-environment-syntax.json"></a>

```
{
  "[Variables](#cfn-lambda-function-environment-variables)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-lambda-function-environment-syntax.yaml"></a>

```
[Variables](#cfn-lambda-function-environment-variables):
  String: String
```

## Properties<a name="w3ab2c21c14e1524b7"></a>

`Variables`  <a name="cfn-lambda-function-environment-variables"></a>
A map of key\-value pairs that the Lambda function can access\.  
*Required*: No  
*Type*: Mapping of key\-value pairs