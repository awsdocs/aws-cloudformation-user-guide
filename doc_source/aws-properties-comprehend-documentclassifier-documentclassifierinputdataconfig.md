# AWS::Comprehend::DocumentClassifier DocumentClassifierInputDataConfig<a name="aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig"></a>

The input properties for training a document classifier\. 

For more information on how the input file is formatted, see [Preparing training data](https://docs.aws.amazon.com/comprehend/latest/dg/prep-classifier-data.html) in the Comprehend Developer Guide\. 

## Syntax<a name="aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig-syntax.json"></a>

```
{
  "[AugmentedManifests](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-augmentedmanifests)" : [ AugmentedManifestsListItem, ... ],
  "[DataFormat](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-dataformat)" : String,
  "[DocumentReaderConfig](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documentreaderconfig)" : DocumentReaderConfig,
  "[Documents](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documents)" : DocumentClassifierDocuments,
  "[DocumentType](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documenttype)" : String,
  "[LabelDelimiter](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-labeldelimiter)" : String,
  "[S3Uri](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-s3uri)" : String,
  "[TestS3Uri](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-tests3uri)" : String
}
```

### YAML<a name="aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig-syntax.yaml"></a>

```
  [AugmentedManifests](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-augmentedmanifests): 
    - AugmentedManifestsListItem
  [DataFormat](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-dataformat): String
  [DocumentReaderConfig](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documentreaderconfig): 
    DocumentReaderConfig
  [Documents](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documents): 
    DocumentClassifierDocuments
  [DocumentType](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documenttype): String
  [LabelDelimiter](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-labeldelimiter): String
  [S3Uri](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-s3uri): String
  [TestS3Uri](#cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-tests3uri): String
```

## Properties<a name="aws-properties-comprehend-documentclassifier-documentclassifierinputdataconfig-properties"></a>

`AugmentedManifests`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-augmentedmanifests"></a>
A list of augmented manifest files that provide training data for your custom model\. An augmented manifest file is a labeled dataset that is produced by Amazon SageMaker Ground Truth\.  
This parameter is required if you set `DataFormat` to `AUGMENTED_MANIFEST`\.  
*Required*: No  
*Type*: List of [AugmentedManifestsListItem](aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataFormat`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-dataformat"></a>
The format of your training data:  
+  `COMPREHEND_CSV`: A two\-column CSV file, where labels are provided in the first column, and documents are provided in the second\. If you use this value, you must provide the `S3Uri` parameter in your request\.
+  `AUGMENTED_MANIFEST`: A labeled dataset that is produced by Amazon SageMaker Ground Truth\. This file is in JSON lines format\. Each line is a complete JSON object that contains a training document and its associated labels\. 

  If you use this value, you must provide the `AugmentedManifests` parameter in your request\.
If you don't specify a value, Amazon Comprehend uses `COMPREHEND_CSV` as the default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUGMENTED_MANIFEST | COMPREHEND_CSV`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentReaderConfig`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documentreaderconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [DocumentReaderConfig](aws-properties-comprehend-documentclassifier-documentreaderconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Documents`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documents"></a>
Property description not available\.  
*Required*: No  
*Type*: [DocumentClassifierDocuments](aws-properties-comprehend-documentclassifier-documentclassifierdocuments.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentType`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-documenttype"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LabelDelimiter`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-labeldelimiter"></a>
Indicates the delimiter used to separate each label for training a multi\-label classifier\. The default delimiter between labels is a pipe \(\|\)\. You can use a different character as a delimiter \(if it's an allowed character\) by specifying it under Delimiter for labels\. If the training documents use a delimiter other than the default or the delimiter you specify, the labels on that line will be combined to make a single unique label, such as LABELLABELLABEL\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1`  
*Pattern*: `^[ ~!@#$%^*\-_+=|\\:;\t>?/]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-s3uri"></a>
The Amazon S3 URI for the input data\. The S3 bucket must be in the same Region as the API endpoint that you are calling\. The URI can point to a single input file or it can provide the prefix for a collection of input files\.  
For example, if you use the URI `S3://bucketName/prefix`, if the prefix is a single file, Amazon Comprehend uses that file as input\. If more than one file begins with the prefix, Amazon Comprehend uses all of them as input\.  
This parameter is required if you set `DataFormat` to `COMPREHEND_CSV`\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `s3://[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9](/.*)?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TestS3Uri`  <a name="cfn-comprehend-documentclassifier-documentclassifierinputdataconfig-tests3uri"></a>
This specifies the Amazon S3 location where the test annotations for an entity recognizer are located\. The URI must be in the same AWS Region as the API endpoint that you are calling\.   
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `s3://[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9](/.*)?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)