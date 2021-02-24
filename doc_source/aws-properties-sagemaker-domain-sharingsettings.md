# AWS::SageMaker::Domain SharingSettings<a name="aws-properties-sagemaker-domain-sharingsettings"></a>

Specifies options when sharing an Amazon SageMaker Studio notebook\. These settings are specified as part of `DefaultUserSettings` when the [CreateDomain](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateDomain.html) API is called, and as part of `UserSettings` when the [CreateUserProfile](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateUserProfile.html) API is called\.

## Syntax<a name="aws-properties-sagemaker-domain-sharingsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-sharingsettings-syntax.json"></a>

```
{
  "[NotebookOutputOption](#cfn-sagemaker-domain-sharingsettings-notebookoutputoption)" : String,
  "[S3KmsKeyId](#cfn-sagemaker-domain-sharingsettings-s3kmskeyid)" : String,
  "[S3OutputPath](#cfn-sagemaker-domain-sharingsettings-s3outputpath)" : String
}
```

### YAML<a name="aws-properties-sagemaker-domain-sharingsettings-syntax.yaml"></a>

```
  [NotebookOutputOption](#cfn-sagemaker-domain-sharingsettings-notebookoutputoption): String
  [S3KmsKeyId](#cfn-sagemaker-domain-sharingsettings-s3kmskeyid): String
  [S3OutputPath](#cfn-sagemaker-domain-sharingsettings-s3outputpath): String
```

## Properties<a name="aws-properties-sagemaker-domain-sharingsettings-properties"></a>

`NotebookOutputOption`  <a name="cfn-sagemaker-domain-sharingsettings-notebookoutputoption"></a>
Whether to include the notebook cell output when sharing the notebook\. The default is `Disabled`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Allowed | Disabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3KmsKeyId`  <a name="cfn-sagemaker-domain-sharingsettings-s3kmskeyid"></a>
When `NotebookOutputOption` is `Allowed`, the AWS Key Management Service \(KMS\) encryption key ID used to encrypt the notebook cell output in the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3OutputPath`  <a name="cfn-sagemaker-domain-sharingsettings-s3outputpath"></a>
When `NotebookOutputOption` is `Allowed`, the Amazon S3 bucket used to store the shared notebook snapshots\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)