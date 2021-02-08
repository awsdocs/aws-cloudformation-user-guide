# AWS::QuickSight::Theme<a name="aws-resource-quicksight-theme"></a>

Creates a theme\.

A *theme* is set of configuration options for color and layout\. Themes apply to analyses and dashboards\. For more information, see [Using Themes in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/themes-in-quicksight.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-resource-quicksight-theme-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-theme-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::Theme",
  "Properties" : {
      "[AwsAccountId](#cfn-quicksight-theme-awsaccountid)" : String,
      "[BaseThemeId](#cfn-quicksight-theme-basethemeid)" : String,
      "[Configuration](#cfn-quicksight-theme-configuration)" : ThemeConfiguration,
      "[Name](#cfn-quicksight-theme-name)" : String,
      "[Permissions](#cfn-quicksight-theme-permissions)" : [ ResourcePermission, ... ],
      "[Tags](#cfn-quicksight-theme-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThemeId](#cfn-quicksight-theme-themeid)" : String,
      "[VersionDescription](#cfn-quicksight-theme-versiondescription)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-theme-syntax.yaml"></a>

```
Type: AWS::QuickSight::Theme
Properties: 
  [AwsAccountId](#cfn-quicksight-theme-awsaccountid): String
  [BaseThemeId](#cfn-quicksight-theme-basethemeid): String
  [Configuration](#cfn-quicksight-theme-configuration): 
    ThemeConfiguration
  [Name](#cfn-quicksight-theme-name): String
  [Permissions](#cfn-quicksight-theme-permissions): 
    - ResourcePermission
  [Tags](#cfn-quicksight-theme-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThemeId](#cfn-quicksight-theme-themeid): String
  [VersionDescription](#cfn-quicksight-theme-versiondescription): String
```

## Properties<a name="aws-resource-quicksight-theme-properties"></a>

`AwsAccountId`  <a name="cfn-quicksight-theme-awsaccountid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BaseThemeId`  <a name="cfn-quicksight-theme-basethemeid"></a>
The Amazon QuickSight\-defined ID of the theme that a custom theme inherits from\. All themes initially inherit from a default QuickSight theme\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-quicksight-theme-configuration"></a>
The theme configuration, which contains all the theme display properties\.  
*Required*: No  
*Type*: [ThemeConfiguration](aws-properties-quicksight-theme-themeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-theme-name"></a>
The name that the user gives to the theme\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-theme-permissions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-theme-resourcepermission.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-theme-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThemeId`  <a name="cfn-quicksight-theme-themeid"></a>
The identifier that the user gives to the theme\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VersionDescription`  <a name="cfn-quicksight-theme-versiondescription"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-theme-return-values"></a>

### Ref<a name="aws-resource-quicksight-theme-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-theme-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-theme-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Type`  <a name="Type-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Version`  <a name="Version-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.