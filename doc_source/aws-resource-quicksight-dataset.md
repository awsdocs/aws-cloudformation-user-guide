# AWS::QuickSight::DataSet<a name="aws-resource-quicksight-dataset"></a>

Creates a dataset\. This operation doesn't support datasets that include uploaded files as a source\.

## Syntax<a name="aws-resource-quicksight-dataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-dataset-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::DataSet",
  "Properties" : {
      "[AwsAccountId](#cfn-quicksight-dataset-awsaccountid)" : String,
      "[ColumnGroups](#cfn-quicksight-dataset-columngroups)" : [ ColumnGroup, ... ],
      "[ColumnLevelPermissionRules](#cfn-quicksight-dataset-columnlevelpermissionrules)" : [ ColumnLevelPermissionRule, ... ],
      "[DataSetId](#cfn-quicksight-dataset-datasetid)" : String,
      "[DataSetUsageConfiguration](#cfn-quicksight-dataset-datasetusageconfiguration)" : DataSetUsageConfiguration,
      "[FieldFolders](#cfn-quicksight-dataset-fieldfolders)" : {Key : Value, ...},
      "[ImportMode](#cfn-quicksight-dataset-importmode)" : String,
      "[IngestionWaitPolicy](#cfn-quicksight-dataset-ingestionwaitpolicy)" : IngestionWaitPolicy,
      "[LogicalTableMap](#cfn-quicksight-dataset-logicaltablemap)" : {Key : Value, ...},
      "[Name](#cfn-quicksight-dataset-name)" : String,
      "[Permissions](#cfn-quicksight-dataset-permissions)" : [ ResourcePermission, ... ],
      "[PhysicalTableMap](#cfn-quicksight-dataset-physicaltablemap)" : {Key : Value, ...},
      "[RowLevelPermissionDataSet](#cfn-quicksight-dataset-rowlevelpermissiondataset)" : RowLevelPermissionDataSet,
      "[Tags](#cfn-quicksight-dataset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-quicksight-dataset-syntax.yaml"></a>

```
Type: AWS::QuickSight::DataSet
Properties: 
  [AwsAccountId](#cfn-quicksight-dataset-awsaccountid): String
  [ColumnGroups](#cfn-quicksight-dataset-columngroups): 
    - ColumnGroup
  [ColumnLevelPermissionRules](#cfn-quicksight-dataset-columnlevelpermissionrules): 
    - ColumnLevelPermissionRule
  [DataSetId](#cfn-quicksight-dataset-datasetid): String
  [DataSetUsageConfiguration](#cfn-quicksight-dataset-datasetusageconfiguration): 
    DataSetUsageConfiguration
  [FieldFolders](#cfn-quicksight-dataset-fieldfolders): 
    Key : Value
  [ImportMode](#cfn-quicksight-dataset-importmode): String
  [IngestionWaitPolicy](#cfn-quicksight-dataset-ingestionwaitpolicy): 
    IngestionWaitPolicy
  [LogicalTableMap](#cfn-quicksight-dataset-logicaltablemap): 
    Key : Value
  [Name](#cfn-quicksight-dataset-name): String
  [Permissions](#cfn-quicksight-dataset-permissions): 
    - ResourcePermission
  [PhysicalTableMap](#cfn-quicksight-dataset-physicaltablemap): 
    Key : Value
  [RowLevelPermissionDataSet](#cfn-quicksight-dataset-rowlevelpermissiondataset): 
    RowLevelPermissionDataSet
  [Tags](#cfn-quicksight-dataset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-quicksight-dataset-properties"></a>

`AwsAccountId`  <a name="cfn-quicksight-dataset-awsaccountid"></a>
The AWS account ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ColumnGroups`  <a name="cfn-quicksight-dataset-columngroups"></a>
Groupings of columns that work together in certain Amazon QuickSight features\. Currently, only geospatial hierarchy is supported\.  
*Required*: No  
*Type*: List of [ColumnGroup](aws-properties-quicksight-dataset-columngroup.md)  
*Maximum*: `8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnLevelPermissionRules`  <a name="cfn-quicksight-dataset-columnlevelpermissionrules"></a>
A set of one or more definitions of a ` ColumnLevelPermissionRule `\.  
*Required*: No  
*Type*: List of [ColumnLevelPermissionRule](aws-properties-quicksight-dataset-columnlevelpermissionrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetId`  <a name="cfn-quicksight-dataset-datasetid"></a>
An ID for the dataset that you want to create\. This ID is unique per AWS Region for each AWS account\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSetUsageConfiguration`  <a name="cfn-quicksight-dataset-datasetusageconfiguration"></a>
The usage configuration to apply to child datasets that reference this dataset as a source\.  
*Required*: No  
*Type*: [DataSetUsageConfiguration](aws-properties-quicksight-dataset-datasetusageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldFolders`  <a name="cfn-quicksight-dataset-fieldfolders"></a>
The folder that contains fields and nested subfolders for your dataset\.  
*Required*: No  
*Type*: Map of [FieldFolder](aws-properties-quicksight-dataset-fieldfolder.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImportMode`  <a name="cfn-quicksight-dataset-importmode"></a>
Indicates whether you want to import the data into SPICE\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIRECT_QUERY | SPICE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngestionWaitPolicy`  <a name="cfn-quicksight-dataset-ingestionwaitpolicy"></a>
The wait policy to use when creating or updating a Dataset\. The default is to wait for SPICE ingestion to finish with timeout of 36 hours\.  
*Required*: No  
*Type*: [IngestionWaitPolicy](aws-properties-quicksight-dataset-ingestionwaitpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalTableMap`  <a name="cfn-quicksight-dataset-logicaltablemap"></a>
Configures the combination and transformation of the data from the physical tables\.  
*Required*: No  
*Type*: Map of [LogicalTable](aws-properties-quicksight-dataset-logicaltable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-name"></a>
The display name for the dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-dataset-permissions"></a>
A list of resource permissions on the dataset\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-dataset-resourcepermission.md)  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhysicalTableMap`  <a name="cfn-quicksight-dataset-physicaltablemap"></a>
Declares the physical tables that are available in the underlying data sources\.  
*Required*: No  
*Type*: Map of [PhysicalTable](aws-properties-quicksight-dataset-physicaltable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowLevelPermissionDataSet`  <a name="cfn-quicksight-dataset-rowlevelpermissiondataset"></a>
The row\-level security configuration for the data that you want to create\.  
*Required*: No  
*Type*: [RowLevelPermissionDataSet](aws-properties-quicksight-dataset-rowlevelpermissiondataset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-dataset-tags"></a>
Contains a map of the key\-value pairs for the resource tag or tags assigned to the dataset\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-dataset-return-values"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-dataset-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-dataset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the dataset\.

`ConsumedSpiceCapacityInBytes`  <a name="ConsumedSpiceCapacityInBytes-fn::getatt"></a>


`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time this dataset version was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The time this dataset version was last updated\.

`OutputColumns`  <a name="OutputColumns-fn::getatt"></a>
