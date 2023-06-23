# AWS::CleanRooms::ConfiguredTable AnalysisRule<a name="aws-properties-cleanrooms-configuredtable-analysisrule"></a>

A specification about how data from the configured table can be used in a query\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-analysisrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-analysisrule-syntax.json"></a>

```
{
  "[Policy](#cfn-cleanrooms-configuredtable-analysisrule-policy)" : ConfiguredTableAnalysisRulePolicy,
  "[Type](#cfn-cleanrooms-configuredtable-analysisrule-type)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-analysisrule-syntax.yaml"></a>

```
  [Policy](#cfn-cleanrooms-configuredtable-analysisrule-policy): 
    ConfiguredTableAnalysisRulePolicy
  [Type](#cfn-cleanrooms-configuredtable-analysisrule-type): String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-analysisrule-properties"></a>

`Policy`  <a name="cfn-cleanrooms-configuredtable-analysisrule-policy"></a>
A policy that describes the associated data usage limitations\.  
*Required*: Yes  
*Type*: [ConfiguredTableAnalysisRulePolicy](aws-properties-cleanrooms-configuredtable-configuredtableanalysisrulepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-cleanrooms-configuredtable-analysisrule-type"></a>
The type of analysis rule\. Valid values are `AGGREGATION` and `LIST`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)