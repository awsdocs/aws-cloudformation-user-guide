# AWS::Glue::Classifier CsvClassifier<a name="aws-properties-glue-classifier-csvclassifier"></a>

A classifier for custom `CSV` content\.

## Syntax<a name="aws-properties-glue-classifier-csvclassifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-classifier-csvclassifier-syntax.json"></a>

```
{
  "[AllowSingleColumn](#cfn-glue-classifier-csvclassifier-allowsinglecolumn)" : Boolean,
  "[ContainsHeader](#cfn-glue-classifier-csvclassifier-containsheader)" : String,
  "[Delimiter](#cfn-glue-classifier-csvclassifier-delimiter)" : String,
  "[DisableValueTrimming](#cfn-glue-classifier-csvclassifier-disablevaluetrimming)" : Boolean,
  "[Header](#cfn-glue-classifier-csvclassifier-header)" : [ String, ... ],
  "[Name](#cfn-glue-classifier-csvclassifier-name)" : String,
  "[QuoteSymbol](#cfn-glue-classifier-csvclassifier-quotesymbol)" : String
}
```

### YAML<a name="aws-properties-glue-classifier-csvclassifier-syntax.yaml"></a>

```
  [AllowSingleColumn](#cfn-glue-classifier-csvclassifier-allowsinglecolumn): Boolean
  [ContainsHeader](#cfn-glue-classifier-csvclassifier-containsheader): String
  [Delimiter](#cfn-glue-classifier-csvclassifier-delimiter): String
  [DisableValueTrimming](#cfn-glue-classifier-csvclassifier-disablevaluetrimming): Boolean
  [Header](#cfn-glue-classifier-csvclassifier-header): 
    - String
  [Name](#cfn-glue-classifier-csvclassifier-name): String
  [QuoteSymbol](#cfn-glue-classifier-csvclassifier-quotesymbol): String
```

## Properties<a name="aws-properties-glue-classifier-csvclassifier-properties"></a>

`AllowSingleColumn`  <a name="cfn-glue-classifier-csvclassifier-allowsinglecolumn"></a>
Enables the processing of files that contain only one column\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainsHeader`  <a name="cfn-glue-classifier-csvclassifier-containsheader"></a>
Indicates whether the CSV file contains a header\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Delimiter`  <a name="cfn-glue-classifier-csvclassifier-delimiter"></a>
A custom symbol to denote what separates each column entry in the row\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableValueTrimming`  <a name="cfn-glue-classifier-csvclassifier-disablevaluetrimming"></a>
Specifies not to trim values before identifying the type of column values\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-glue-classifier-csvclassifier-header"></a>
A list of strings representing column names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-classifier-csvclassifier-name"></a>
The name of the classifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QuoteSymbol`  <a name="cfn-glue-classifier-csvclassifier-quotesymbol"></a>
A custom symbol to denote what combines content into a single column value\. It must be different from the column delimiter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-glue-classifier-csvclassifier--examples"></a>



### Create a custom classifier test<a name="aws-properties-glue-classifier-csvclassifier--examples--Create_a_custom_classifier_test"></a>

With `AWS::Glue::Classifier` you can create a custom classifier test\.

#### JSON<a name="aws-properties-glue-classifier-csvclassifier--examples--Create_a_custom_classifier_test--json"></a>

```
{
    "Description": "AWS Glue Custom Classifier Test",
    "Resources": {
        "MyCSVclassifier": {
            "Type": "AWS::Glue::Classifier",
            "Properties": {
                "CsvClassifier": {
                    "AllowSingleColumn": true,
                    "ContainsHeader": "PRESENT",
                    "Delimiter": ",",
                    "Header": [
                        "id",
                        "name"
                    ],
                    "Name": "csvclassify",
                    "QuoteSymbol": "\""
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-glue-classifier-csvclassifier--examples--Create_a_custom_classifier_test--yaml"></a>

```
Description: AWS Glue Custom Classifier Test
Resources:
  MyCSVclassifier:
    Type: 'AWS::Glue::Classifier'
    Properties:
      CsvClassifier:
        AllowSingleColumn: true
        ContainsHeader: PRESENT
        Delimiter: ','
        Header:
          - id
          - name
        Name: csvclassify
        QuoteSymbol: '"'
```