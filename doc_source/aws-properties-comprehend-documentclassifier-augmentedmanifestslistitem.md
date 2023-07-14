# AWS::Comprehend::DocumentClassifier AugmentedManifestsListItem<a name="aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem"></a>

An augmented manifest file that provides training data for your custom model\. An augmented manifest file is a labeled dataset that is produced by Amazon SageMaker Ground Truth\.

## Syntax<a name="aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem-syntax.json"></a>

```
{
  "[AttributeNames](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-attributenames)" : [ String, ... ],
  "[S3Uri](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-s3uri)" : String,
  "[Split](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-split)" : String
}
```

### YAML<a name="aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem-syntax.yaml"></a>

```
  [AttributeNames](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-attributenames): 
    - String
  [S3Uri](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-s3uri): String
  [Split](#cfn-comprehend-documentclassifier-augmentedmanifestslistitem-split): String
```

## Properties<a name="aws-properties-comprehend-documentclassifier-augmentedmanifestslistitem-properties"></a>

`AttributeNames`  <a name="cfn-comprehend-documentclassifier-augmentedmanifestslistitem-attributenames"></a>
The JSON attribute that contains the annotations for your training documents\. The number of attribute names that you specify depends on whether your augmented manifest file is the output of a single labeling job or a chained labeling job\.  
If your file is the output of a single labeling job, specify the LabelAttributeName key that was used when the job was created in Ground Truth\.  
If your file is the output of a chained labeling job, specify the LabelAttributeName key for one or more jobs in the chain\. Each LabelAttributeName key provides the annotations from an individual job\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-comprehend-documentclassifier-augmentedmanifestslistitem-s3uri"></a>
The Amazon S3 location of the augmented manifest file\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `s3://[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9](/.*)?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Split`  <a name="cfn-comprehend-documentclassifier-augmentedmanifestslistitem-split"></a>
The purpose of the data you've provided in the augmented manifest\. You can either train or test this data\. If you don't specify, the default is train\.  
TRAIN \- all of the documents in the manifest will be used for training\. If no test documents are provided, Amazon Comprehend will automatically reserve a portion of the training documents for testing\.  
 TEST \- all of the documents in the manifest will be used for testing\.  
*Required*: No  
*Type*: String  
*Allowed values*: `TEST | TRAIN`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)