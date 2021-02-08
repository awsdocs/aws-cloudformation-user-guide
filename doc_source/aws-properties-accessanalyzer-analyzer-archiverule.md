# AWS::AccessAnalyzer::Analyzer ArchiveRule<a name="aws-properties-accessanalyzer-analyzer-archiverule"></a>

The criteria for an archive rule\.

## Syntax<a name="aws-properties-accessanalyzer-analyzer-archiverule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-accessanalyzer-analyzer-archiverule-syntax.json"></a>

```
{
  "[Filter](#cfn-accessanalyzer-analyzer-archiverule-filter)" : [ Filter, ... ],
  "[RuleName](#cfn-accessanalyzer-analyzer-archiverule-rulename)" : String
}
```

### YAML<a name="aws-properties-accessanalyzer-analyzer-archiverule-syntax.yaml"></a>

```
  [Filter](#cfn-accessanalyzer-analyzer-archiverule-filter): 
    - Filter
  [RuleName](#cfn-accessanalyzer-analyzer-archiverule-rulename): String
```

## Properties<a name="aws-properties-accessanalyzer-analyzer-archiverule-properties"></a>

`Filter`  <a name="cfn-accessanalyzer-analyzer-archiverule-filter"></a>
The criteria for the rule\.  
*Required*: Yes  
*Type*: [List](aws-properties-accessanalyzer-analyzer-filter.md) of [Filter](aws-properties-accessanalyzer-analyzer-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleName`  <a name="cfn-accessanalyzer-analyzer-archiverule-rulename"></a>
The name of the archive rule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)