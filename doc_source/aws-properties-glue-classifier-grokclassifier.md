# AWS Glue Classifier GrokClassifier<a name="aws-properties-glue-classifier-grokclassifier"></a>

<a name="aws-properties-glue-classifier-grokclassifier-description"></a>The `GrokClassifier` property type specifies an AWS Glue classifier that uses `grok`\.

<a name="aws-properties-glue-classifier-grokclassifier-inheritance"></a> `GrokClassifier` is a property of the [AWS::Glue::Classifier](aws-resource-glue-classifier.md) resource\.

## Syntax<a name="aws-properties-glue-classifier-grokclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-classifier-grokclassifier-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-custompatterns)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-grokpattern)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-classification)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-name)" : String
}
```

### YAML<a name="aws-properties-glue-classifier-grokclassifier-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-custompatterns): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-grokpattern): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-classification): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-classifier-grokclassifier-name): String
```

## Properties<a name="aws-properties-glue-classifier-grokclassifier-properties"></a>

For more information, see [GrokClassifier Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-GrokClassifier) in the *AWS Glue Developer Guide*\.

`CustomPatterns`  
Custom grok patterns that are used by this classifier\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`GrokPattern`  
The grok pattern that's used by this classifier\. It must match the Logstash grok string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Classification`  
The data form that the classifier matches—such as Twitter, JSON, or Omniture logs\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The name of the classifier\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 