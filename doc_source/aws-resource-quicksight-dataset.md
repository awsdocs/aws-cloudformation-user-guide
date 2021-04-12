# AWS::QuickSight::DataSet<a name="aws-resource-quicksight-dataset"></a>

Creates a dataset\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
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
The ID of the dataset\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FieldFolders`  <a name="cfn-quicksight-dataset-fieldfolders"></a>
The folder that contains fields and nested subfolders for your dataset\.  
*Required*: No  
*Type*: Map of [FieldFolder](aws-properties-quicksight-dataset-fieldfolder.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImportMode`  <a name="cfn-quicksight-dataset-importmode"></a>
A value that indicates whether you want to import the data into SPICE\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIRECT_QUERY | SPICE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngestionWaitPolicy`  <a name="cfn-quicksight-dataset-ingestionwaitpolicy"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [IngestionWaitPolicy](aws-properties-quicksight-dataset-ingestionwaitpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalTableMap`  <a name="cfn-quicksight-dataset-logicaltablemap"></a>
Configures the combination and transformation of the data from the physical tables\.  
*Required*: No  
*Type*: Map of [LogicalTable](aws-properties-quicksight-dataset-logicaltable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-name"></a>
A display name for the dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-dataset-permissions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-dataset-resourcepermission.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhysicalTableMap`  <a name="cfn-quicksight-dataset-physicaltablemap"></a>
Declares the physical tables that are available in the underlying data sources\.  
*Required*: No  
*Type*: Map of [PhysicalTable](aws-properties-quicksight-dataset-physicaltable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowLevelPermissionDataSet`  <a name="cfn-quicksight-dataset-rowlevelpermissiondataset"></a>
The row\-level security configuration for the dataset\.  
*Required*: No  
*Type*: [RowLevelPermissionDataSet](aws-properties-quicksight-dataset-rowlevelpermissiondataset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-dataset-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-dataset-return-values"></a>

### Ref<a name="aws-resource-quicksight-dataset-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-dataset-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-dataset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ConsumedSpiceCapacityInBytes`  <a name="ConsumedSpiceCapacityInBytes-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`OutputColumns`  <a name="OutputColumns-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.