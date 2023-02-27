# AWS::SageMaker::ModelPackage TransformOutput<a name="aws-properties-sagemaker-modelpackage-transformoutput"></a>

Describes the results of a transform job\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-transformoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-transformoutput-syntax.json"></a>

```
{
  "[Accept](#cfn-sagemaker-modelpackage-transformoutput-accept)" : String,
  "[AssembleWith](#cfn-sagemaker-modelpackage-transformoutput-assemblewith)" : String,
  "[KmsKeyId](#cfn-sagemaker-modelpackage-transformoutput-kmskeyid)" : String,
  "[S3OutputPath](#cfn-sagemaker-modelpackage-transformoutput-s3outputpath)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-transformoutput-syntax.yaml"></a>

```
  [Accept](#cfn-sagemaker-modelpackage-transformoutput-accept): String
  [AssembleWith](#cfn-sagemaker-modelpackage-transformoutput-assemblewith): String
  [KmsKeyId](#cfn-sagemaker-modelpackage-transformoutput-kmskeyid): String
  [S3OutputPath](#cfn-sagemaker-modelpackage-transformoutput-s3outputpath): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-transformoutput-properties"></a>

`Accept`  <a name="cfn-sagemaker-modelpackage-transformoutput-accept"></a>
The MIME type used to specify the output data\. Amazon SageMaker uses the MIME type with each http call to transfer data from the transform job\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AssembleWith`  <a name="cfn-sagemaker-modelpackage-transformoutput-assemblewith"></a>
Defines how to assemble the results of the transform job as a single S3 object\. Choose a format that is most convenient to you\. To concatenate the results in binary format, specify `None`\. To add a newline character at the end of every transformed record, specify `Line`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Line | None`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-sagemaker-modelpackage-transformoutput-kmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt the model artifacts at rest using Amazon S3 server\-side encryption\. The `KmsKeyId` can be any of the following formats:   
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Key ARN: `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Alias name: `alias/ExampleAlias` 
+ Alias name ARN: `arn:aws:kms:us-west-2:111122223333:alias/ExampleAlias` 
If you don't provide a KMS key ID, Amazon SageMaker uses the default KMS key for Amazon S3 for your role's account\. For more information, see [KMS\-Managed Encryption Keys](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html) in the *Amazon Simple Storage Service Developer Guide\.*   
The KMS key policy must grant permission to the IAM role that you specify in your [CreateModel](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateModel.html) request\. For more information, see [Using Key Policies in AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/key-policies.html) in the * AWS Key Management Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3OutputPath`  <a name="cfn-sagemaker-modelpackage-transformoutput-s3outputpath"></a>
The Amazon S3 path where you want Amazon SageMaker to store the results of the transform job\. For example, `s3://bucket-name/key-name-prefix`\.  
For every S3 object used as input for the transform job, batch transform stores the transformed data with an \.`out` suffix in a corresponding subfolder in the location in the output prefix\. For example, for the input data stored at `s3://bucket-name/input-name-prefix/dataset01/data.csv`, batch transform stores the transformed data at `s3://bucket-name/output-name-prefix/input-name-prefix/data.csv.out`\. Batch transform doesn't upload partially processed objects\. For an input S3 object that contains multiple records, it creates an \.`out` file only if the transform job succeeds on the entire file\. When the input contains multiple S3 objects, the batch transform job processes the listed S3 objects and uploads only the output for successfully processed objects\. If any object fails in the transform job batch transform marks the job as failed to prompt investigation\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)