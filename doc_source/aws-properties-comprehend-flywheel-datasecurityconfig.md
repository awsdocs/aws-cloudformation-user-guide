# AWS::Comprehend::Flywheel DataSecurityConfig<a name="aws-properties-comprehend-flywheel-datasecurityconfig"></a>

Data security configuration\.

## Syntax<a name="aws-properties-comprehend-flywheel-datasecurityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-flywheel-datasecurityconfig-syntax.json"></a>

```
{
  "[DataLakeKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-datalakekmskeyid)" : String,
  "[ModelKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-modelkmskeyid)" : String,
  "[VolumeKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-volumekmskeyid)" : String,
  "[VpcConfig](#cfn-comprehend-flywheel-datasecurityconfig-vpcconfig)" : VpcConfig
}
```

### YAML<a name="aws-properties-comprehend-flywheel-datasecurityconfig-syntax.yaml"></a>

```
  [DataLakeKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-datalakekmskeyid): String
  [ModelKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-modelkmskeyid): String
  [VolumeKmsKeyId](#cfn-comprehend-flywheel-datasecurityconfig-volumekmskeyid): String
  [VpcConfig](#cfn-comprehend-flywheel-datasecurityconfig-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-properties-comprehend-flywheel-datasecurityconfig-properties"></a>

`DataLakeKmsKeyId`  <a name="cfn-comprehend-flywheel-datasecurityconfig-datalakekmskeyid"></a>
ID for the AWS KMS key that Amazon Comprehend uses to encrypt the data in the data lake\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^\p{ASCII}+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelKmsKeyId`  <a name="cfn-comprehend-flywheel-datasecurityconfig-modelkmskeyid"></a>
ID for the AWS KMS key that Amazon Comprehend uses to encrypt trained custom models\. The ModelKmsKeyId can be either of the following formats:  
+ KMS Key ID: `"1234abcd-12ab-34cd-56ef-1234567890ab"` 
+ Amazon Resource Name \(ARN\) of a KMS Key: `"arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab"` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^\p{ASCII}+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeKmsKeyId`  <a name="cfn-comprehend-flywheel-datasecurityconfig-volumekmskeyid"></a>
ID for the AWS KMS key that Amazon Comprehend uses to encrypt the volume\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^\p{ASCII}+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-comprehend-flywheel-datasecurityconfig-vpcconfig"></a>
 Configuration parameters for an optional private Virtual Private Cloud \(VPC\) containing the resources you are using for the job\. For more information, see [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)\.   
*Required*: No  
*Type*: [VpcConfig](aws-properties-comprehend-flywheel-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)