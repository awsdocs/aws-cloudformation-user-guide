# AWS::AppRunner::Service SourceCodeVersion<a name="aws-properties-apprunner-service-sourcecodeversion"></a>

Identifies a version of code that AWS App Runner refers to within a source code repository\.

## Syntax<a name="aws-properties-apprunner-service-sourcecodeversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-sourcecodeversion-syntax.json"></a>

```
{
  "[Type](#cfn-apprunner-service-sourcecodeversion-type)" : String,
  "[Value](#cfn-apprunner-service-sourcecodeversion-value)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-sourcecodeversion-syntax.yaml"></a>

```
  [Type](#cfn-apprunner-service-sourcecodeversion-type): String
  [Value](#cfn-apprunner-service-sourcecodeversion-value): String
```

## Properties<a name="aws-properties-apprunner-service-sourcecodeversion-properties"></a>

`Type`  <a name="cfn-apprunner-service-sourcecodeversion-type"></a>
The type of version identifier\.  
For a git\-based repository, branches represent versions\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BRANCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-apprunner-service-sourcecodeversion-value"></a>
A source code version\.  
For a git\-based repository, a branch name maps to a specific version\. App Runner uses the most recent commit to the branch\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `51200`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)