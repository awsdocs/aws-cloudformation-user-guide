# AWS::CleanRooms::ConfiguredTable AnalysisRuleCustom<a name="aws-properties-cleanrooms-configuredtable-analysisrulecustom"></a>

A type of analysis rule that enables the table owner to approve custom SQL queries on their configured tables\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-analysisrulecustom-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-analysisrulecustom-syntax.json"></a>

```
{
  "[AllowedAnalyses](#cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalyses)" : [ String, ... ],
  "[AllowedAnalysisProviders](#cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalysisproviders)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-analysisrulecustom-syntax.yaml"></a>

```
  [AllowedAnalyses](#cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalyses): 
    - String
  [AllowedAnalysisProviders](#cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalysisproviders): 
    - String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-analysisrulecustom-properties"></a>

`AllowedAnalyses`  <a name="cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalyses"></a>
The analysis templates that are allowed by the custom analysis rule\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedAnalysisProviders`  <a name="cfn-cleanrooms-configuredtable-analysisrulecustom-allowedanalysisproviders"></a>
The AWS accounts that are allowed to query by the custom analysis rule\. Required when `allowedAnalyses` is `ANY_QUERY`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)