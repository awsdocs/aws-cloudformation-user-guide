# AWS::SageMaker::DeviceFleet EdgeOutputConfig<a name="aws-properties-sagemaker-devicefleet-edgeoutputconfig"></a>

The output configuration\.

## Syntax<a name="aws-properties-sagemaker-devicefleet-edgeoutputconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-devicefleet-edgeoutputconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-devicefleet-edgeoutputconfig-kmskeyid)" : String,
  "[S3OutputLocation](#cfn-sagemaker-devicefleet-edgeoutputconfig-s3outputlocation)" : String
}
```

### YAML<a name="aws-properties-sagemaker-devicefleet-edgeoutputconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-devicefleet-edgeoutputconfig-kmskeyid): String
  [S3OutputLocation](#cfn-sagemaker-devicefleet-edgeoutputconfig-s3outputlocation): String
```

## Properties<a name="aws-properties-sagemaker-devicefleet-edgeoutputconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-devicefleet-edgeoutputconfig-kmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt data on the storage volume after compilation job\. If you don't provide a KMS key ID, Amazon SageMaker uses the default KMS key for Amazon S3 for your role's account\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3OutputLocation`  <a name="cfn-sagemaker-devicefleet-edgeoutputconfig-s3outputlocation"></a>
The Amazon Simple Storage \(S3\) bucker URI\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)