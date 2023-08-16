# AWS::SageMaker::ModelPackage TransformResources<a name="aws-properties-sagemaker-modelpackage-transformresources"></a>

Describes the resources, including ML instance types and ML instance count, to use for transform job\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-transformresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-transformresources-syntax.json"></a>

```
{
  "[InstanceCount](#cfn-sagemaker-modelpackage-transformresources-instancecount)" : Integer,
  "[InstanceType](#cfn-sagemaker-modelpackage-transformresources-instancetype)" : String,
  "[VolumeKmsKeyId](#cfn-sagemaker-modelpackage-transformresources-volumekmskeyid)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-transformresources-syntax.yaml"></a>

```
  [InstanceCount](#cfn-sagemaker-modelpackage-transformresources-instancecount): Integer
  [InstanceType](#cfn-sagemaker-modelpackage-transformresources-instancetype): String
  [VolumeKmsKeyId](#cfn-sagemaker-modelpackage-transformresources-volumekmskeyid): String
```

## Properties<a name="aws-properties-sagemaker-modelpackage-transformresources-properties"></a>

`InstanceCount`  <a name="cfn-sagemaker-modelpackage-transformresources-instancecount"></a>
The number of ML compute instances to use in the transform job\. The default value is `1`, and the maximum is `100`\. For distributed transform jobs, specify a value greater than `1`\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-sagemaker-modelpackage-transformresources-instancetype"></a>
The ML compute instance type for the transform job\. If you are using built\-in algorithms to transform moderately sized datasets, we recommend using ml\.m4\.xlarge or `ml.m5.large`instance types\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ml.c4.2xlarge | ml.c4.4xlarge | ml.c4.8xlarge | ml.c4.xlarge | ml.c5.18xlarge | ml.c5.2xlarge | ml.c5.4xlarge | ml.c5.9xlarge | ml.c5.xlarge | ml.g4dn.12xlarge | ml.g4dn.16xlarge | ml.g4dn.2xlarge | ml.g4dn.4xlarge | ml.g4dn.8xlarge | ml.g4dn.xlarge | ml.m4.10xlarge | ml.m4.16xlarge | ml.m4.2xlarge | ml.m4.4xlarge | ml.m4.xlarge | ml.m5.12xlarge | ml.m5.24xlarge | ml.m5.2xlarge | ml.m5.4xlarge | ml.m5.large | ml.m5.xlarge | ml.p2.16xlarge | ml.p2.8xlarge | ml.p2.xlarge | ml.p3.16xlarge | ml.p3.2xlarge | ml.p3.8xlarge`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeKmsKeyId`  <a name="cfn-sagemaker-modelpackage-transformresources-volumekmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt model data on the storage volume attached to the ML compute instance\(s\) that run the batch transform job\.  
Certain Nitro\-based instances include local storage, dependent on the instance type\. Local storage volumes are encrypted using a hardware module on the instance\. You can't request a `VolumeKmsKeyId` when using an instance type with local storage\.  
For a list of instance types that support local instance storage, see [Instance Store Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html#instance-store-volumes)\.  
For more information about local instance storage encryption, see [SSD Instance Store Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ssd-instance-store.html)\.
 The `VolumeKmsKeyId` can be any of the following formats:  
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Key ARN: `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab` 
+ Alias name: `alias/ExampleAlias` 
+ Alias name ARN: `arn:aws:kms:us-west-2:111122223333:alias/ExampleAlias` 
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)