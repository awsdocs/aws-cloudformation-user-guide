# AWS::Lambda::Function TracingConfig<a name="aws-properties-lambda-function-tracingconfig"></a>

The function's AWS X\-Ray tracing configuration\. To sample and record incoming requests, set `Mode` to `Active`\.

## Syntax<a name="aws-properties-lambda-function-tracingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-tracingconfig-syntax.json"></a>

```
{
  "[Mode](#cfn-lambda-function-tracingconfig-mode)" : String
}
```

### YAML<a name="aws-properties-lambda-function-tracingconfig-syntax.yaml"></a>

```
  [Mode](#cfn-lambda-function-tracingconfig-mode): String
```

## Properties<a name="aws-properties-lambda-function-tracingconfig-properties"></a>

`Mode`  <a name="cfn-lambda-function-tracingconfig-mode"></a>
The tracing mode\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Active | PassThrough`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-function-tracingconfig--examples"></a>

### Tracing Configuration<a name="aws-properties-lambda-function-tracingconfig--examples--Tracing_Configuration"></a>

Enable active tracing on a function\.

#### YAML<a name="aws-properties-lambda-function-tracingconfig--examples--Tracing_Configuration--yaml"></a>

```
      TracingConfig:
        Mode: Active
```