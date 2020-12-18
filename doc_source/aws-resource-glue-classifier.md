# AWS::Glue::Classifier<a name="aws-resource-glue-classifier"></a>

The `AWS::Glue::Classifier` resource creates an AWS Glue classifier that categorizes data sources and specifies schemas\. For more information, see [Adding Classifiers to a Crawler](https://docs.aws.amazon.com/glue/latest/dg/add-classifier.html) and [Classifier Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-classifiers.html#aws-glue-api-crawler-classifiers-Classifier) in the *AWS Glue Developer Guide*\. 

## Syntax<a name="aws-resource-glue-classifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-classifier-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Classifier",
  "Properties" : {
      "[CsvClassifier](#cfn-glue-classifier-csvclassifier)" : CsvClassifier,
      "[GrokClassifier](#cfn-glue-classifier-grokclassifier)" : GrokClassifier,
      "[JsonClassifier](#cfn-glue-classifier-jsonclassifier)" : JsonClassifier,
      "[XMLClassifier](#cfn-glue-classifier-xmlclassifier)" : XMLClassifier
    }
}
```

### YAML<a name="aws-resource-glue-classifier-syntax.yaml"></a>

```
Type: AWS::Glue::Classifier
Properties: 
  [CsvClassifier](#cfn-glue-classifier-csvclassifier): 
    CsvClassifier
  [GrokClassifier](#cfn-glue-classifier-grokclassifier): 
    GrokClassifier
  [JsonClassifier](#cfn-glue-classifier-jsonclassifier): 
    JsonClassifier
  [XMLClassifier](#cfn-glue-classifier-xmlclassifier): 
    XMLClassifier
```

## Properties<a name="aws-resource-glue-classifier-properties"></a>

`CsvClassifier`  <a name="cfn-glue-classifier-csvclassifier"></a>
A classifier for comma\-separated values \(CSV\)\.  
*Required*: Conditional  
*Type*: [CsvClassifier](aws-properties-glue-classifier-csvclassifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrokClassifier`  <a name="cfn-glue-classifier-grokclassifier"></a>
A classifier that uses `grok`\.  
*Required*: Conditional  
*Type*: [GrokClassifier](aws-properties-glue-classifier-grokclassifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonClassifier`  <a name="cfn-glue-classifier-jsonclassifier"></a>
A classifier for JSON content\.  
*Required*: Conditional  
*Type*: [JsonClassifier](aws-properties-glue-classifier-jsonclassifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XMLClassifier`  <a name="cfn-glue-classifier-xmlclassifier"></a>
A classifier for XML content\.  
*Required*: Conditional  
*Type*: [XMLClassifier](aws-properties-glue-classifier-xmlclassifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-classifier-return-values"></a>

### Ref<a name="aws-resource-glue-classifier-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the classifier name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.