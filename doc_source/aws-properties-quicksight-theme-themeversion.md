# AWS::QuickSight::Theme ThemeVersion<a name="aws-properties-quicksight-theme-themeversion"></a>

A version of a theme\.

## Syntax<a name="aws-properties-quicksight-theme-themeversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-themeversion-syntax.json"></a>

```
{
  "[Arn](#cfn-quicksight-theme-themeversion-arn)" : String,
  "[BaseThemeId](#cfn-quicksight-theme-themeversion-basethemeid)" : String,
  "[Configuration](#cfn-quicksight-theme-themeversion-configuration)" : ThemeConfiguration,
  "[CreatedTime](#cfn-quicksight-theme-themeversion-createdtime)" : String,
  "[Description](#cfn-quicksight-theme-themeversion-description)" : String,
  "[Errors](#cfn-quicksight-theme-themeversion-errors)" : [ ThemeError, ... ],
  "[Status](#cfn-quicksight-theme-themeversion-status)" : String,
  "[VersionNumber](#cfn-quicksight-theme-themeversion-versionnumber)" : Double
}
```

### YAML<a name="aws-properties-quicksight-theme-themeversion-syntax.yaml"></a>

```
  [Arn](#cfn-quicksight-theme-themeversion-arn): String
  [BaseThemeId](#cfn-quicksight-theme-themeversion-basethemeid): String
  [Configuration](#cfn-quicksight-theme-themeversion-configuration): 
    ThemeConfiguration
  [CreatedTime](#cfn-quicksight-theme-themeversion-createdtime): String
  [Description](#cfn-quicksight-theme-themeversion-description): String
  [Errors](#cfn-quicksight-theme-themeversion-errors): 
    - ThemeError
  [Status](#cfn-quicksight-theme-themeversion-status): String
  [VersionNumber](#cfn-quicksight-theme-themeversion-versionnumber): Double
```

## Properties<a name="aws-properties-quicksight-theme-themeversion-properties"></a>

`Arn`  <a name="cfn-quicksight-theme-themeversion-arn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseThemeId`  <a name="cfn-quicksight-theme-themeversion-basethemeid"></a>
The Amazon QuickSight\-defined ID of the theme that a custom theme inherits from\. All themes initially inherit from a default Amazon QuickSight theme\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-quicksight-theme-themeversion-configuration"></a>
The theme configuration, which contains all the theme display properties\.  
*Required*: No  
*Type*: [ThemeConfiguration](aws-properties-quicksight-theme-themeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedTime`  <a name="cfn-quicksight-theme-themeversion-createdtime"></a>
The date and time that this theme version was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-quicksight-theme-themeversion-description"></a>
The description of the theme\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Errors`  <a name="cfn-quicksight-theme-themeversion-errors"></a>
Errors associated with the theme\.  
*Required*: No  
*Type*: List of [ThemeError](aws-properties-quicksight-theme-themeerror.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-theme-themeversion-status"></a>
The status of the theme version\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CREATION_FAILED | CREATION_IN_PROGRESS | CREATION_SUCCESSFUL | DELETED | UPDATE_FAILED | UPDATE_IN_PROGRESS | UPDATE_SUCCESSFUL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionNumber`  <a name="cfn-quicksight-theme-themeversion-versionnumber"></a>
The version number of the theme\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)