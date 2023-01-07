# AWS::Glue::Classifier XMLClassifier<a name="aws-properties-glue-classifier-xmlclassifier"></a>

A classifier for `XML` content\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-classifier-xmlclassifier-name"></a>
The name of the classifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RowTag`  <a name="cfn-glue-classifier-xmlclassifier-rowtag"></a>
The XML tag designating the element that contains each record in an XML document being parsed\. This can't identify a self\-closing element \(closed by `/>`\)\. An empty row element that contains only attributes can be parsed as long as it ends with a closing tag \(for example, `<row item_a="A" item_b="B"></row>` is okay, but `<row item_a="A" item_b="B" />` is not\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-glue-classifier-xmlclassifier--seealso"></a>
+  [XMLClassifier Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-XMLClassifier) in the *AWS Glue Developer Guide* 

