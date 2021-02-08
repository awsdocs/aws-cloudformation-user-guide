# AWS::ApplicationInsights::Application LogPattern<a name="aws-properties-applicationinsights-application-logpattern"></a>

The `AWS::ApplicationInsights::Application LogPattern` property type specifies an object that defines the log patterns that belong to a `LogPatternSet`\.

## Syntax<a name="aws-properties-applicationinsights-application-logpattern-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-logpattern-syntax.json"></a>

```
{
  "[Pattern](#cfn-applicationinsights-application-logpattern-pattern)" : String,
  "[PatternName](#cfn-applicationinsights-application-logpattern-patternname)" : String,
  "[Rank](#cfn-applicationinsights-application-logpattern-rank)" : Integer
}
```

### YAML<a name="aws-properties-applicationinsights-application-logpattern-syntax.yaml"></a>

```
  [Pattern](#cfn-applicationinsights-application-logpattern-pattern): String
  [PatternName](#cfn-applicationinsights-application-logpattern-patternname): String
  [Rank](#cfn-applicationinsights-application-logpattern-rank): Integer
```

## Properties<a name="aws-properties-applicationinsights-application-logpattern-properties"></a>

`Pattern`  <a name="cfn-applicationinsights-application-logpattern-pattern"></a>
A regular expression that defines the log pattern\. A log pattern can contain up to 50 characters, and it cannot be empty\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\S\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternName`  <a name="cfn-applicationinsights-application-logpattern-patternname"></a>
The name of the log pattern\. A log pattern name can contain up to 50 characters, and it cannot be empty\. The characters can be Unicode letters, digits, or one of the following symbols: period, dash, underscore\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[a-zA-Z0-9\.\-_]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rank`  <a name="cfn-applicationinsights-application-logpattern-rank"></a>
The rank of the log pattern\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)