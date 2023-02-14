# AWS::AmplifyUIBuilder::Theme ThemeValue<a name="aws-properties-amplifyuibuilder-theme-themevalue"></a>

The `ThemeValue` property specifies the configuration of a theme's properties\.

## Syntax<a name="aws-properties-amplifyuibuilder-theme-themevalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-theme-themevalue-syntax.json"></a>

```
{
  "[Children](#cfn-amplifyuibuilder-theme-themevalue-children)" : [ ThemeValues, ... ],
  "[Value](#cfn-amplifyuibuilder-theme-themevalue-value)" : String
}
```

### YAML<a name="aws-properties-amplifyuibuilder-theme-themevalue-syntax.yaml"></a>

```
  [Children](#cfn-amplifyuibuilder-theme-themevalue-children): 
    - ThemeValues
  [Value](#cfn-amplifyuibuilder-theme-themevalue-value): String
```

## Properties<a name="aws-properties-amplifyuibuilder-theme-themevalue-properties"></a>

`Children`  <a name="cfn-amplifyuibuilder-theme-themevalue-children"></a>
A list of key\-value pairs that define the theme's properties\.  
*Required*: No  
*Type*: List of [ThemeValues](aws-properties-amplifyuibuilder-theme-themevalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amplifyuibuilder-theme-themevalue-value"></a>
The value of a theme property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)