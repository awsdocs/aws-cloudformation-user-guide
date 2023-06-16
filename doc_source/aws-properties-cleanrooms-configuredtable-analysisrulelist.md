# AWS::CleanRooms::ConfiguredTable AnalysisRuleList<a name="aws-properties-cleanrooms-configuredtable-analysisrulelist"></a>

A type of analysis rule that enables row\-level analysis\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-analysisrulelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-analysisrulelist-syntax.json"></a>

```
{
  "[JoinColumns](#cfn-cleanrooms-configuredtable-analysisrulelist-joincolumns)" : [ String, ... ],
  "[ListColumns](#cfn-cleanrooms-configuredtable-analysisrulelist-listcolumns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-analysisrulelist-syntax.yaml"></a>

```
  [JoinColumns](#cfn-cleanrooms-configuredtable-analysisrulelist-joincolumns): 
    - String
  [ListColumns](#cfn-cleanrooms-configuredtable-analysisrulelist-listcolumns): 
    - String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-analysisrulelist-properties"></a>

`JoinColumns`  <a name="cfn-cleanrooms-configuredtable-analysisrulelist-joincolumns"></a>
Columns that can be used to join a configured table with the table of the member who can query and other members' configured tables\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListColumns`  <a name="cfn-cleanrooms-configuredtable-analysisrulelist-listcolumns"></a>
Columns that can be listed in the output\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)