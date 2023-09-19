# AWS::QuickSight::DataSet RowLevelPermissionTagConfiguration<a name="aws-properties-quicksight-dataset-rowlevelpermissiontagconfiguration"></a>

The element you can use to define tags for row\-level security\.

## Syntax<a name="aws-properties-quicksight-dataset-rowlevelpermissiontagconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-rowlevelpermissiontagconfiguration-syntax.json"></a>

```
{
  "[Status](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-status)" : String,
  "[TagRuleConfigurations](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagruleconfigurations)" : Json,
  "[TagRules](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagrules)" : [ RowLevelPermissionTagRule, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-rowlevelpermissiontagconfiguration-syntax.yaml"></a>

```
  [Status](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-status): String
  [TagRuleConfigurations](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagruleconfigurations): Json
  [TagRules](#cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagrules): 
    - RowLevelPermissionTagRule
```

## Properties<a name="aws-properties-quicksight-dataset-rowlevelpermissiontagconfiguration-properties"></a>

`Status`  <a name="cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-status"></a>
The status of row\-level security tags\. If enabled, the status is `ENABLED`\. If disabled, the status is `DISABLED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagRuleConfigurations`  <a name="cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagruleconfigurations"></a>
The configuration of tags on a dataset to set row\-level security\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagRules`  <a name="cfn-quicksight-dataset-rowlevelpermissiontagconfiguration-tagrules"></a>
A set of rules associated with row\-level security, such as the tag names and columns that they are assigned to\.  
*Required*: Yes  
*Type*: List of [RowLevelPermissionTagRule](aws-properties-quicksight-dataset-rowlevelpermissiontagrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)