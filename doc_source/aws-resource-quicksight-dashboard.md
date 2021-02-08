# AWS::QuickSight::Dashboard<a name="aws-resource-quicksight-dashboard"></a>

Creates a dashboard from a template\. To first create a template, see the ` CreateTemplate ` API operation\.

A dashboard is an entity in QuickSight that identifies QuickSight reports, created from analyses\. You can share QuickSight dashboards\. With the right permissions, you can create scheduled email reports from them\. If you have the correct permissions, you can create a dashboard from a template that exists in a different AWS account\.

## Syntax<a name="aws-resource-quicksight-dashboard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-dashboard-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::Dashboard",
  "Properties" : {
      "[AwsAccountId](#cfn-quicksight-dashboard-awsaccountid)" : String,
      "[DashboardId](#cfn-quicksight-dashboard-dashboardid)" : String,
      "[DashboardPublishOptions](#cfn-quicksight-dashboard-dashboardpublishoptions)" : DashboardPublishOptions,
      "[Name](#cfn-quicksight-dashboard-name)" : String,
      "[Parameters](#cfn-quicksight-dashboard-parameters)" : Parameters,
      "[Permissions](#cfn-quicksight-dashboard-permissions)" : [ ResourcePermission, ... ],
      "[SourceEntity](#cfn-quicksight-dashboard-sourceentity)" : DashboardSourceEntity,
      "[Tags](#cfn-quicksight-dashboard-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThemeArn](#cfn-quicksight-dashboard-themearn)" : String,
      "[VersionDescription](#cfn-quicksight-dashboard-versiondescription)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-dashboard-syntax.yaml"></a>

```
Type: AWS::QuickSight::Dashboard
Properties: 
  [AwsAccountId](#cfn-quicksight-dashboard-awsaccountid): String
  [DashboardId](#cfn-quicksight-dashboard-dashboardid): String
  [DashboardPublishOptions](#cfn-quicksight-dashboard-dashboardpublishoptions): 
    DashboardPublishOptions
  [Name](#cfn-quicksight-dashboard-name): String
  [Parameters](#cfn-quicksight-dashboard-parameters): 
    Parameters
  [Permissions](#cfn-quicksight-dashboard-permissions): 
    - ResourcePermission
  [SourceEntity](#cfn-quicksight-dashboard-sourceentity): 
    DashboardSourceEntity
  [Tags](#cfn-quicksight-dashboard-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThemeArn](#cfn-quicksight-dashboard-themearn): String
  [VersionDescription](#cfn-quicksight-dashboard-versiondescription): String
```

## Properties<a name="aws-resource-quicksight-dashboard-properties"></a>

`AwsAccountId`  <a name="cfn-quicksight-dashboard-awsaccountid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DashboardId`  <a name="cfn-quicksight-dashboard-dashboardid"></a>
Dashboard ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DashboardPublishOptions`  <a name="cfn-quicksight-dashboard-dashboardpublishoptions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DashboardPublishOptions](aws-properties-quicksight-dashboard-dashboardpublishoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-name"></a>
A display name for the dashboard\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-quicksight-dashboard-parameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Parameters](aws-properties-quicksight-dashboard-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-dashboard-permissions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-dashboard-resourcepermission.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEntity`  <a name="cfn-quicksight-dashboard-sourceentity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DashboardSourceEntity](aws-properties-quicksight-dashboard-dashboardsourceentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-dashboard-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThemeArn`  <a name="cfn-quicksight-dashboard-themearn"></a>
The ARN of the theme associated with a version of the dashboard\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionDescription`  <a name="cfn-quicksight-dashboard-versiondescription"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-dashboard-return-values"></a>

### Ref<a name="aws-resource-quicksight-dashboard-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-dashboard-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-dashboard-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastPublishedTime`  <a name="LastPublishedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Version`  <a name="Version-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.