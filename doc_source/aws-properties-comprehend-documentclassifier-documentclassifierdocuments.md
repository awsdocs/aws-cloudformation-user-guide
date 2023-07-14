# AWS::Comprehend::DocumentClassifier DocumentClassifierDocuments<a name="aws-properties-comprehend-documentclassifier-documentclassifierdocuments"></a>

The location of the training documents\. This parameter is required in a request to create a native document model\.

## Syntax<a name="aws-properties-comprehend-documentclassifier-documentclassifierdocuments-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-documentclassifier-documentclassifierdocuments-syntax.json"></a>

```
{
  "[S3Uri](#cfn-comprehend-documentclassifier-documentclassifierdocuments-s3uri)" : String,
  "[TestS3Uri](#cfn-comprehend-documentclassifier-documentclassifierdocuments-tests3uri)" : String
}
```

### YAML<a name="aws-properties-comprehend-documentclassifier-documentclassifierdocuments-syntax.yaml"></a>

```
  [S3Uri](#cfn-comprehend-documentclassifier-documentclassifierdocuments-s3uri): String
  [TestS3Uri](#cfn-comprehend-documentclassifier-documentclassifierdocuments-tests3uri): String
```

## Properties<a name="aws-properties-comprehend-documentclassifier-documentclassifierdocuments-properties"></a>

`S3Uri`  <a name="cfn-comprehend-documentclassifier-documentclassifierdocuments-s3uri"></a>
The S3 URI location of the training documents specified in the S3Uri CSV file\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `s3://[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9](/.*)?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TestS3Uri`  <a name="cfn-comprehend-documentclassifier-documentclassifierdocuments-tests3uri"></a>
The S3 URI location of the test documents included in the TestS3Uri CSV file\. This field is not required if you do not specify a test CSV file\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `s3://[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9](/.*)?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)