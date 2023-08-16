# AWS::Lambda::Function SnapStartResponse<a name="aws-properties-lambda-function-snapstartresponse"></a>

The function's [SnapStart](https://docs.aws.amazon.com/lambda/latest/dg/snapstart.html) setting\.

## Syntax<a name="aws-properties-lambda-function-snapstartresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-snapstartresponse-syntax.json"></a>

```
{
  "[ApplyOn](#cfn-lambda-function-snapstartresponse-applyon)" : String,
  "[OptimizationStatus](#cfn-lambda-function-snapstartresponse-optimizationstatus)" : String
}
```

### YAML<a name="aws-properties-lambda-function-snapstartresponse-syntax.yaml"></a>

```
  [ApplyOn](#cfn-lambda-function-snapstartresponse-applyon): String
  [OptimizationStatus](#cfn-lambda-function-snapstartresponse-optimizationstatus): String
```

## Properties<a name="aws-properties-lambda-function-snapstartresponse-properties"></a>

`ApplyOn`  <a name="cfn-lambda-function-snapstartresponse-applyon"></a>
When set to `PublishedVersions`, Lambda creates a snapshot of the execution environment when you publish a function version\.  
*Required*: No  
*Type*: String  
*Allowed values*: `None | PublishedVersions`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptimizationStatus`  <a name="cfn-lambda-function-snapstartresponse-optimizationstatus"></a>
When you provide a [qualified Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/lambda/latest/dg/configuration-versions.html#versioning-versions-using), this response element indicates whether SnapStart is activated for the specified function version\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Off | On`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)