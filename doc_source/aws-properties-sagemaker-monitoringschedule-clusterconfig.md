# AWS::SageMaker::MonitoringSchedule ClusterConfig<a name="aws-properties-sagemaker-monitoringschedule-clusterconfig"></a>

Configuration for the cluster used to run model monitoring jobs\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-clusterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-clusterconfig-syntax.json"></a>

```
{
  "[InstanceCount](#cfn-sagemaker-monitoringschedule-clusterconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-sagemaker-monitoringschedule-clusterconfig-instancetype)" : String,
  "[VolumeKmsKeyId](#cfn-sagemaker-monitoringschedule-clusterconfig-volumekmskeyid)" : String,
  "[VolumeSizeInGB](#cfn-sagemaker-monitoringschedule-clusterconfig-volumesizeingb)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-clusterconfig-syntax.yaml"></a>

```
  [InstanceCount](#cfn-sagemaker-monitoringschedule-clusterconfig-instancecount): Integer
  [InstanceType](#cfn-sagemaker-monitoringschedule-clusterconfig-instancetype): String
  [VolumeKmsKeyId](#cfn-sagemaker-monitoringschedule-clusterconfig-volumekmskeyid): String
  [VolumeSizeInGB](#cfn-sagemaker-monitoringschedule-clusterconfig-volumesizeingb): Integer
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-clusterconfig-properties"></a>

`InstanceCount`  <a name="cfn-sagemaker-monitoringschedule-clusterconfig-instancecount"></a>
The number of ML compute instances to use in the model monitoring job\. For distributed processing jobs, specify a value greater than 1\. The default value is 1\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-sagemaker-monitoringschedule-clusterconfig-instancetype"></a>
The ML compute instance type for the processing job\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeKmsKeyId`  <a name="cfn-sagemaker-monitoringschedule-clusterconfig-volumekmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt data on the storage volume attached to the ML compute instance\(s\) that run the model monitoring job\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSizeInGB`  <a name="cfn-sagemaker-monitoringschedule-clusterconfig-volumesizeingb"></a>
The size of the ML storage volume, in gigabytes, that you want to provision\. You must specify sufficient ML storage for your scenario\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)