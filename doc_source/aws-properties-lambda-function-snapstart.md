# AWS::Lambda::Function SnapStart<a name="aws-properties-lambda-function-snapstart"></a>

The function's [AWS Lambda SnapStart](https://docs.aws.amazon.com/lambda/latest/dg/snapstart.html) setting\.

## Syntax<a name="aws-properties-lambda-function-snapstart-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-snapstart-syntax.json"></a>

```
{
  "[ApplyOn](#cfn-lambda-function-snapstart-applyon)" : String
}
```

### YAML<a name="aws-properties-lambda-function-snapstart-syntax.yaml"></a>

```
  [ApplyOn](#cfn-lambda-function-snapstart-applyon): String
```

## Properties<a name="aws-properties-lambda-function-snapstart-properties"></a>

`ApplyOn`  <a name="cfn-lambda-function-snapstart-applyon"></a>
Set `ApplyOn` to `PublishedVersions` to create a snapshot of the initialized execution environment when you publish a function version\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `None | PublishedVersions`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)