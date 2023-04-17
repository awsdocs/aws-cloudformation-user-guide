# AWS::SageMaker::FeatureGroup S3StorageConfig<a name="aws-properties-sagemaker-featuregroup-s3storageconfig"></a>

The Amazon Simple Storage \(Amazon S3\) location and and security configuration for `OfflineStore`\.

## Syntax<a name="aws-properties-sagemaker-featuregroup-s3storageconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-featuregroup-s3storageconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-featuregroup-s3storageconfig-kmskeyid)" : String,
  "[S3Uri](#cfn-sagemaker-featuregroup-s3storageconfig-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-featuregroup-s3storageconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-featuregroup-s3storageconfig-kmskeyid): String
  [S3Uri](#cfn-sagemaker-featuregroup-s3storageconfig-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-featuregroup-s3storageconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-featuregroup-s3storageconfig-kmskeyid"></a>
The AWS Key Management Service \(KMS\) key ARN of the key used to encrypt any objects written into the `OfflineStore` S3 location\.  
The IAM `roleARN` that is passed as a parameter to `CreateFeatureGroup` must have below permissions to the `KmsKeyId`:  
+  `"kms:GenerateDataKey"` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-sagemaker-featuregroup-s3storageconfig-s3uri"></a>
The S3 URI, or location in Amazon S3, of `OfflineStore`\.  
S3 URIs have a format similar to the following: `s3://example-bucket/prefix/`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)