# AWS::CleanRooms::AnalysisTemplate AnalysisSchema<a name="aws-properties-cleanrooms-analysistemplate-analysisschema"></a>

A relation within an analysis\.

## Syntax<a name="aws-properties-cleanrooms-analysistemplate-analysisschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-analysistemplate-analysisschema-syntax.json"></a>

```
{
  "[ReferencedTables](#cfn-cleanrooms-analysistemplate-analysisschema-referencedtables)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cleanrooms-analysistemplate-analysisschema-syntax.yaml"></a>

```
  [ReferencedTables](#cfn-cleanrooms-analysistemplate-analysisschema-referencedtables): 
    - String
```

## Properties<a name="aws-properties-cleanrooms-analysistemplate-analysisschema-properties"></a>

`ReferencedTables`  <a name="cfn-cleanrooms-analysistemplate-analysisschema-referencedtables"></a>
The tables referenced in the analysis schema\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: Updates are not supported\.