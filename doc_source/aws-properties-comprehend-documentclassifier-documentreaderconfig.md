# AWS::Comprehend::DocumentClassifier DocumentReaderConfig<a name="aws-properties-comprehend-documentclassifier-documentreaderconfig"></a>

Provides configuration parameters to override the default actions for extracting text from PDF documents and image files\. 

 By default, Amazon Comprehend performs the following actions to extract text from files, based on the input file type: 
+  **Word files** \- Amazon Comprehend parser extracts the text\. 
+  **Digital PDF files** \- Amazon Comprehend parser extracts the text\. 
+  **Image files and scanned PDF files** \- Amazon Comprehend uses the Amazon Textract `DetectDocumentText` API to extract the text\. 

 `DocumentReaderConfig` does not apply to plain text files or Word files\.

 For image files and PDF documents, you can override these default actions using the fields listed below\. For more information, see [ Setting text extraction options](https://docs.aws.amazon.com/comprehend/latest/dg/idp-set-textract-options.html) in the Comprehend Developer Guide\. 

## Syntax<a name="aws-properties-comprehend-documentclassifier-documentreaderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-documentclassifier-documentreaderconfig-syntax.json"></a>

```
{
  "[DocumentReadAction](#cfn-comprehend-documentclassifier-documentreaderconfig-documentreadaction)" : String,
  "[DocumentReadMode](#cfn-comprehend-documentclassifier-documentreaderconfig-documentreadmode)" : String,
  "[FeatureTypes](#cfn-comprehend-documentclassifier-documentreaderconfig-featuretypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-comprehend-documentclassifier-documentreaderconfig-syntax.yaml"></a>

```
  [DocumentReadAction](#cfn-comprehend-documentclassifier-documentreaderconfig-documentreadaction): String
  [DocumentReadMode](#cfn-comprehend-documentclassifier-documentreaderconfig-documentreadmode): String
  [FeatureTypes](#cfn-comprehend-documentclassifier-documentreaderconfig-featuretypes): 
    - String
```

## Properties<a name="aws-properties-comprehend-documentclassifier-documentreaderconfig-properties"></a>

`DocumentReadAction`  <a name="cfn-comprehend-documentclassifier-documentreaderconfig-documentreadaction"></a>
This field defines the Amazon Textract API operation that Amazon Comprehend uses to extract text from PDF files and image files\. Enter one of the following values:  
+  `TEXTRACT_DETECT_DOCUMENT_TEXT` \- The Amazon Comprehend service uses the `DetectDocumentText` API operation\. 
+  `TEXTRACT_ANALYZE_DOCUMENT` \- The Amazon Comprehend service uses the `AnalyzeDocument` API operation\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `TEXTRACT_ANALYZE_DOCUMENT | TEXTRACT_DETECT_DOCUMENT_TEXT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentReadMode`  <a name="cfn-comprehend-documentclassifier-documentreaderconfig-documentreadmode"></a>
Determines the text extraction actions for PDF files\. Enter one of the following values:  
+  `SERVICE_DEFAULT` \- use the Amazon Comprehend service defaults for PDF files\.
+  `FORCE_DOCUMENT_READ_ACTION` \- Amazon Comprehend uses the Textract API specified by DocumentReadAction for all PDF files, including digital PDF files\. 
*Required*: No  
*Type*: String  
*Allowed values*: `FORCE_DOCUMENT_READ_ACTION | SERVICE_DEFAULT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeatureTypes`  <a name="cfn-comprehend-documentclassifier-documentreaderconfig-featuretypes"></a>
Specifies the type of Amazon Textract features to apply\. If you chose `TEXTRACT_ANALYZE_DOCUMENT` as the read action, you must specify one or both of the following values:  
+  `TABLES` \- Returns information about any tables that are detected in the input document\. 
+  `FORMS` \- Returns information and the data from any forms that are detected in the input document\. 
*Required*: No  
*Type*: List of String  
*Maximum*: `2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)