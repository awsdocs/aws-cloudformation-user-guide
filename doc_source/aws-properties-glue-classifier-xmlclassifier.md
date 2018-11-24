# AWS Glue Classifier XMLClassifier<a name="aws-properties-glue-classifier-xmlclassifier"></a>

<a name="aws-properties-glue-classifier-xmlclassifier-description"></a>The `XMLClassifier` property type specifies specifies an AWS Glue classifier for XML content\.

<a name="aws-properties-glue-classifier-xmlclassifier-inheritance"></a> `XMLClassifier` is a property of the [AWS::Glue::Classifier](aws-resource-glue-classifier.md) resource type\.

## Syntax<a name="aws-properties-glue-classifier-xmlclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-classifier-xmlclassifier-syntax.json"></a>

```
{
  "[Classification](#cfn-glue-classifier-xmlclassifier-classification)" : String,
  "[Name](#cfn-glue-classifier-xmlclassifier-name)" : String,
  "[RowTag](#cfn-glue-classifier-xmlclassifier-rowtag)" : String
}
```

### YAML<a name="aws-properties-glue-classifier-xmlclassifier-syntax.yaml"></a>

```
[Classification](#cfn-glue-classifier-xmlclassifier-classification): String
[Name](#cfn-glue-classifier-xmlclassifier-name): String
[RowTag](#cfn-glue-classifier-xmlclassifier-rowtag): String
```

## Properties<a name="aws-properties-glue-classifier-xmlclassifier-properties"></a>

`Classification`  <a name="cfn-glue-classifier-xmlclassifier-classification"></a>
An identifier of the data format that the classifier matches\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No Interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-classifier-xmlclassifier-name"></a>
The name of the classifier\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RowTag`  <a name="cfn-glue-classifier-xmlclassifier-rowtag"></a>
The XML tag designating the element that contains each record in an XML document being parsed\. Note that this cannot identify a self\-closing element \(closed by />\)\. An empty row element that contains only attributes can be parsed as long as it ends with a closing tag\. For example, `<row item_a="A" item_b="B"></row>` is okay, but `<row item_a="A" item_b="B" />` is not\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No Interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-glue-classifier-xmlclassifier-seealso"></a>
+ [XMLClassifier Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-XMLClassifier) in the *AWS Glue Developer Guide*