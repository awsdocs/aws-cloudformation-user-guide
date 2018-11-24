# AWS Glue Classifier JsonClassifier<a name="aws-properties-glue-classifier-jsonclassifier"></a>

<a name="aws-properties-glue-classifier-jsonclassifier-description"></a>The `JsonClassifier` property type specifies an AWS Glue classifier for JSON content\.

<a name="aws-properties-glue-classifier-jsonclassifier-inheritance"></a> `JsonClassifier` is a property of the [AWS::Glue::Classifier](aws-resource-glue-classifier.md) resource type\.

## Syntax<a name="aws-properties-glue-classifier-jsonclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-classifier-jsonclassifier-syntax.json"></a>

```
{
  "[JsonPath](#cfn-glue-classifier-jsonclassifier-jsonpath)" : String,
  "[Name](#cfn-glue-classifier-jsonclassifier-name)" : String
}
```

### YAML<a name="aws-properties-glue-classifier-jsonclassifier-syntax.yaml"></a>

```
[JsonPath](#cfn-glue-classifier-jsonclassifier-jsonpath): String
[Name](#cfn-glue-classifier-jsonclassifier-name): String
```

## Properties<a name="aws-properties-glue-classifier-jsonclassifier-properties"></a>

`JsonPath`  <a name="cfn-glue-classifier-jsonclassifier-jsonpath"></a>
A JsonPath string defining the JSON data for the classifier to classify\. AWS Glue supports a subset of JsonPath, as described in [Writing JsonPath Custom Classifiers](https://docs.aws.amazon.com/glue/latest/dg/custom-classifier.html#custom-classifier-json)\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No Interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-classifier-jsonclassifier-name"></a>
The name of the classifier\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-glue-classifier-jsonclassifier-seealso"></a>
+ [JsonClassifier Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-JsonClassifier) in the *AWS Glue Developer Guide*