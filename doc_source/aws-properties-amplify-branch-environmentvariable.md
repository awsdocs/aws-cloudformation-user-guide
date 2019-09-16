# AWS::Amplify::Branch EnvironmentVariable<a name="aws-properties-amplify-branch-environmentvariable"></a>

The EnvironmentVariable property type sets environment variables for a specific branch\. Environment variables are key\-value pairs that are available at build time\.

## Syntax<a name="aws-properties-amplify-branch-environmentvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-branch-environmentvariable-syntax.json"></a>

```
{
  "[Name](#cfn-amplify-branch-environmentvariable-name)" : String,
  "[Value](#cfn-amplify-branch-environmentvariable-value)" : String
}
```

### YAML<a name="aws-properties-amplify-branch-environmentvariable-syntax.yaml"></a>

```
  [Name](#cfn-amplify-branch-environmentvariable-name): String
  [Value](#cfn-amplify-branch-environmentvariable-value): String
```

## Properties<a name="aws-properties-amplify-branch-environmentvariable-properties"></a>

`Name`  <a name="cfn-amplify-branch-environmentvariable-name"></a>
The environment variable name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amplify-branch-environmentvariable-value"></a>
The environment variable value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)