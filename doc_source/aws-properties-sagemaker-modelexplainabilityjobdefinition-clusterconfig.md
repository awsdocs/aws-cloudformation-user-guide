# AWS::SageMaker::ModelExplainabilityJobDefinition ClusterConfig<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig"></a>

The configuration for the cluster resources used to run the processing job\.

## Syntax<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig-syntax.json"></a>

```
{
  "[InstanceCount](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancetype)" : String,
  "[VolumeKmsKeyId](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumekmskeyid)" : String,
  "[VolumeSizeInGB](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumesizeingb)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig-syntax.yaml"></a>

```
  [InstanceCount](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancecount): Integer
  [InstanceType](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancetype): String
  [VolumeKmsKeyId](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumekmskeyid): String
  [VolumeSizeInGB](#cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumesizeingb): Integer
```

## Properties<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-clusterconfig-properties"></a>

`InstanceCount`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancecount"></a>
The number of ML compute instances to use in the model monitoring job\. For distributed processing jobs, specify a value greater than 1\. The default value is 1\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-instancetype"></a>
The ML compute instance type for the processing job\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeKmsKeyId`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumekmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt data on the storage volume attached to the ML compute instance\(s\) that run the model monitoring job\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeSizeInGB`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-clusterconfig-volumesizeingb"></a>
The size of the ML storage volume, in gigabytes, that you want to provision\. You must specify sufficient ML storage for your scenario\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)