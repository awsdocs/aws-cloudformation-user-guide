# AWS::SageMaker::FeatureGroup OnlineStoreSecurityConfig<a name="aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig"></a>

The security configuration for `OnlineStore`\.

## Syntax<a name="aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-featuregroup-onlinestoresecurityconfig-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-featuregroup-onlinestoresecurityconfig-kmskeyid): String
```

## Properties<a name="aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-featuregroup-onlinestoresecurityconfig-kmskeyid"></a>
The AWS Key Management Service \(KMS\) key ARN that SageMaker Feature Store uses to encrypt the Amazon S3 objects at rest using Amazon S3 server\-side encryption\.  
The caller \(either user or IAM role\) of `CreateFeatureGroup` must have below permissions to the `OnlineStore` `KmsKeyId`:  
+  `"kms:Encrypt"` 
+  `"kms:Decrypt"` 
+  `"kms:DescribeKey"` 
+  `"kms:CreateGrant"` 
+  `"kms:RetireGrant"` 
+  `"kms:ReEncryptFrom"` 
+  `"kms:ReEncryptTo"` 
+  `"kms:GenerateDataKey"` 
+  `"kms:ListAliases"` 
+  `"kms:ListGrants"` 
+  `"kms:RevokeGrant"` 
The caller \(either user or IAM role\) to all DataPlane operations \(`PutRecord`, `GetRecord`, `DeleteRecord`\) must have the following permissions to the `KmsKeyId`:  
+  `"kms:Decrypt"` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)