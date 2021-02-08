# AWS::ApplicationInsights::Application LogPatternSet<a name="aws-properties-applicationinsights-application-logpatternset"></a>

The `AWS::ApplicationInsights::Application LogPatternSet` property type specifies the log pattern set\.

## Syntax<a name="aws-properties-applicationinsights-application-logpatternset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-logpatternset-syntax.json"></a>

```
{
  "[LogPatterns](#cfn-applicationinsights-application-logpatternset-logpatterns)" : [ LogPattern, ... ],
  "[PatternSetName](#cfn-applicationinsights-application-logpatternset-patternsetname)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-logpatternset-syntax.yaml"></a>

```
  [LogPatterns](#cfn-applicationinsights-application-logpatternset-logpatterns): 
    - LogPattern
  [PatternSetName](#cfn-applicationinsights-application-logpatternset-patternsetname): String
```

## Properties<a name="aws-properties-applicationinsights-application-logpatternset-properties"></a>

`LogPatterns`  <a name="cfn-applicationinsights-application-logpatternset-logpatterns"></a>
A list of objects that define the log patterns that belong to `LogPatternSet`\.  
*Required*: Yes  
*Type*: List of [LogPattern](aws-properties-applicationinsights-application-logpattern.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternSetName`  <a name="cfn-applicationinsights-application-logpatternset-patternsetname"></a>
The name of the log pattern\. A log pattern name can contain up to 30 characters, and it cannot be empty\. The characters can be Unicode letters, digits, or one of the following symbols: period, dash, underscore\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Pattern*: `[a-zA-Z0-9\.\-_]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)