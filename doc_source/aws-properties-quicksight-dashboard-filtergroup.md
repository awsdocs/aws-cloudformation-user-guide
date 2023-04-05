# AWS::QuickSight::Dashboard FilterGroup<a name="aws-properties-quicksight-dashboard-filtergroup"></a>

A grouping of individual filters\. Filter groups are applied to the same group of visuals\.

For more information, see [Adding filter conditions \(group filters\) with AND and OR operators](https://docs.aws.amazon.com/quicksight/latest/user/add-a-compound-filter.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-dashboard-filtergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filtergroup-syntax.json"></a>

```
{
  "[CrossDataset](#cfn-quicksight-dashboard-filtergroup-crossdataset)" : String,
  "[FilterGroupId](#cfn-quicksight-dashboard-filtergroup-filtergroupid)" : String,
  "[Filters](#cfn-quicksight-dashboard-filtergroup-filters)" : [ Filter, ... ],
  "[ScopeConfiguration](#cfn-quicksight-dashboard-filtergroup-scopeconfiguration)" : FilterScopeConfiguration,
  "[Status](#cfn-quicksight-dashboard-filtergroup-status)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filtergroup-syntax.yaml"></a>

```
  [CrossDataset](#cfn-quicksight-dashboard-filtergroup-crossdataset): String
  [FilterGroupId](#cfn-quicksight-dashboard-filtergroup-filtergroupid): String
  [Filters](#cfn-quicksight-dashboard-filtergroup-filters): 
    - Filter
  [ScopeConfiguration](#cfn-quicksight-dashboard-filtergroup-scopeconfiguration): 
    FilterScopeConfiguration
  [Status](#cfn-quicksight-dashboard-filtergroup-status): String
```

## Properties<a name="aws-properties-quicksight-dashboard-filtergroup-properties"></a>

`CrossDataset`  <a name="cfn-quicksight-dashboard-filtergroup-crossdataset"></a>
The filter new feature which can apply filter group to all data sets\. Choose one of the following options:  
+  `ALL_DATASETS` 
+  `SINGLE_DATASET` 
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_DATASETS | SINGLE_DATASET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterGroupId`  <a name="cfn-quicksight-dashboard-filtergroup-filtergroupid"></a>
The value that uniquely identifies a `FilterGroup` within a dashboard, template, or analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filters`  <a name="cfn-quicksight-dashboard-filtergroup-filters"></a>
The list of filters that are present in a `FilterGroup`\.  
*Required*: Yes  
*Type*: List of [Filter](aws-properties-quicksight-dashboard-filter.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeConfiguration`  <a name="cfn-quicksight-dashboard-filtergroup-scopeconfiguration"></a>
The configuration that specifies what scope to apply to a `FilterGroup`\.  
This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.  
*Required*: Yes  
*Type*: [FilterScopeConfiguration](aws-properties-quicksight-dashboard-filterscopeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-dashboard-filtergroup-status"></a>
The status of the `FilterGroup`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)