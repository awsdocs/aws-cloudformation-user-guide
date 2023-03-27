# AWS::QuickSight::Dashboard<a name="aws-resource-quicksight-dashboard"></a>

Creates a dashboard from a template\. To first create a template, see the `CreateTemplate` API operation\.

A dashboard is an entity in Amazon QuickSight that identifies Amazon QuickSight reports, created from analyses\. You can share Amazon QuickSight dashboards\. With the right permissions, you can create scheduled email reports from them\. If you have the correct permissions, you can create a dashboard from a template that exists in a different AWS account\.

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
The ID of the AWS account where you want to create the dashboard\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DashboardId`  <a name="cfn-quicksight-dashboard-dashboardid"></a>
The ID for the dashboard, also added to the IAM policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DashboardPublishOptions`  <a name="cfn-quicksight-dashboard-dashboardpublishoptions"></a>
Options for publishing the dashboard when you create it:  
+  `AvailabilityStatus` for `AdHocFilteringOption` \- This status can be either `ENABLED` or `DISABLED`\. When this is set to `DISABLED`, Amazon QuickSight disables the left filter pane on the published dashboard, which can be used for ad hoc \(one\-time\) filtering\. This option is `ENABLED` by default\. 
+  `AvailabilityStatus` for `ExportToCSVOption` \- This status can be either `ENABLED` or `DISABLED`\. The visual option to export data to \.CSV format isn't enabled when this is set to `DISABLED`\. This option is `ENABLED` by default\. 
+  `VisibilityState` for `SheetControlsOption` \- This visibility state can be either `COLLAPSED` or `EXPANDED`\. This option is `COLLAPSED` by default\. 
*Required*: No  
*Type*: [DashboardPublishOptions](aws-properties-quicksight-dashboard-dashboardpublishoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-name"></a>
The display name of the dashboard\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-quicksight-dashboard-parameters"></a>
The parameters for the creation of the dashboard, which you want to use to override the default settings\. A dashboard can have any type of parameters, and some parameters might accept multiple values\.   
*Required*: No  
*Type*: [Parameters](aws-properties-quicksight-dashboard-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-dashboard-permissions"></a>
A structure that contains the permissions of the dashboard\. You can use this structure for granting permissions by providing a list of IAM action information for each principal ARN\.   
To specify no permissions, omit the permissions list\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-dashboard-resourcepermission.md)  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEntity`  <a name="cfn-quicksight-dashboard-sourceentity"></a>
The entity that you are using as a source when you create the dashboard\. In `SourceEntity`, you specify the type of object that you want to use\. You can only create a dashboard from a template, so you use a `SourceTemplate` entity\. If you need to create a dashboard from an analysis, first convert the analysis to a template by using the `CreateTemplate` API operation\. For `SourceTemplate`, specify the Amazon Resource Name \(ARN\) of the source template\. The `SourceTemplate`ARN can contain any AWS account; and any QuickSight\-supported AWS Region\.   
Use the `DataSetReferences` entity within `SourceTemplate` to list the replacement datasets for the placeholders listed in the original\. The schema in each dataset must match its placeholder\.   
*Required*: Yes  
*Type*: [DashboardSourceEntity](aws-properties-quicksight-dashboard-dashboardsourceentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-dashboard-tags"></a>
Contains a map of the key\-value pairs for the resource tag or tags assigned to the dashboard\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThemeArn`  <a name="cfn-quicksight-dashboard-themearn"></a>
The Amazon Resource Name \(ARN\) of the theme that is being used for this dashboard\. If you add a value for this field, it overrides the value that is used in the source entity\. The theme ARN must exist in the same AWS account where you create the dashboard\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionDescription`  <a name="cfn-quicksight-dashboard-versiondescription"></a>
A description for the first version of the dashboard being created\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-dashboard-return-values"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-dashboard-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-dashboard-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the dashboard\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time this dashboard version was created\.

`LastPublishedTime`  <a name="LastPublishedTime-fn::getatt"></a>
The time that the dashboard was last published\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The time that the dashboard was last updated\.

`Version`  <a name="Version-fn::getatt"></a>
The version of the dashboard\.

`Version.Arn`  <a name="Version.Arn-fn::getatt"></a>
Property description not available\.

`Version.CreatedTime`  <a name="Version.CreatedTime-fn::getatt"></a>
Property description not available\.

`Version.DataSetArns`  <a name="Version.DataSetArns-fn::getatt"></a>
Property description not available\.

`Version.Description`  <a name="Version.Description-fn::getatt"></a>
Property description not available\.

`Version.Errors`  <a name="Version.Errors-fn::getatt"></a>
Property description not available\.

`Version.Sheets`  <a name="Version.Sheets-fn::getatt"></a>
Property description not available\.

`Version.SourceEntityArn`  <a name="Version.SourceEntityArn-fn::getatt"></a>
Property description not available\.

`Version.Status`  <a name="Version.Status-fn::getatt"></a>
Property description not available\.

`Version.ThemeArn`  <a name="Version.ThemeArn-fn::getatt"></a>
Property description not available\.

`Version.VersionNumber`  <a name="Version.VersionNumber-fn::getatt"></a>
Property description not available\.