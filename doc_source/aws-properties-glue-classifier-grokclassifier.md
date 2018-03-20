# AWS Glue Classifier GrokClassifier<a name="aws-properties-glue-classifier-grokclassifier"></a>

<a name="aws-properties-glue-classifier-grokclassifier-description"></a>The `GrokClassifier` property type specifies an AWS Glue classifier that uses `grok`\.

<a name="aws-properties-glue-classifier-grokclassifier-inheritance"></a> `GrokClassifier` is a property of the [AWS::Glue::Classifier](aws-resource-glue-classifier.md) resource\.

## Syntax<a name="aws-properties-glue-classifier-grokclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-classifier-grokclassifier-syntax.json"></a>

```
{
  "[CustomPatterns](#cfn-glue-classifier-grokclassifier-custompatterns)" : String,
  "[GrokPattern](#cfn-glue-classifier-grokclassifier-grokpattern)" : String,
  "[Classification](#cfn-glue-classifier-grokclassifier-classification)" : String,
  "[Name](#cfn-glue-classifier-grokclassifier-name)" : String
}
```

### YAML<a name="aws-properties-glue-classifier-grokclassifier-syntax.yaml"></a>

```
[CustomPatterns](#cfn-glue-classifier-grokclassifier-custompatterns): String
[GrokPattern](#cfn-glue-classifier-grokclassifier-grokpattern): String
[Classification](#cfn-glue-classifier-grokclassifier-classification): String
[Name](#cfn-glue-classifier-grokclassifier-name): String
```

## Properties<a name="aws-properties-glue-classifier-grokclassifier-properties"></a>

For more information, see [GrokClassifier Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-GrokClassifier) in the *AWS Glue Developer Guide*\.

`CustomPatterns`  <a name="cfn-glue-classifier-grokclassifier-custompatterns"></a>
Custom grok patterns that are used by this classifier\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`GrokPattern`  <a name="cfn-glue-classifier-grokclassifier-grokpattern"></a>
The grok pattern that's used by this classifier\. It must match the Logstash grok string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Classification`  <a name="cfn-glue-classifier-grokclassifier-classification"></a>
The data form that the classifier matches—such as Twitter, JSON, or Omniture logs\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-classifier-grokclassifier-name"></a>
The name of the classifier\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 