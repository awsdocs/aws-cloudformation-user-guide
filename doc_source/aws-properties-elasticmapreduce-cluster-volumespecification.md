# AWS::EMR::Cluster VolumeSpecification<a name="aws-properties-elasticmapreduce-cluster-volumespecification"></a>

`VolumeSpecification` is a subproperty of the `EbsBlockDeviceConfig` property type\. `VolumeSecification` determines the volume type, IOPS, and size \(GiB\) for EBS volumes attached to EC2 instances\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-volumespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-volumespecification-syntax.json"></a>

```
{
  "[Iops](#cfn-elasticmapreduce-cluster-volumespecification-iops)" : Integer,
  "[SizeInGB](#cfn-elasticmapreduce-cluster-volumespecification-sizeingb)" : Integer,
  "[VolumeType](#cfn-elasticmapreduce-cluster-volumespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-volumespecification-syntax.yaml"></a>

```
  [Iops](#cfn-elasticmapreduce-cluster-volumespecification-iops): Integer
  [SizeInGB](#cfn-elasticmapreduce-cluster-volumespecification-sizeingb): Integer
  [VolumeType](#cfn-elasticmapreduce-cluster-volumespecification-volumetype): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-volumespecification-properties"></a>

`Iops`  <a name="cfn-elasticmapreduce-cluster-volumespecification-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. IOPS parameters are supported for volumes: io1 and gp3\. Among them, IOPS parameters are required for volumes io1 but optional for volumes gp3 which default to 3000 IOPS\. IOPS parameters are not supported for volumes: gp2, standard, st1 and sc1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeInGB`  <a name="cfn-elasticmapreduce-cluster-volumespecification-sizeingb"></a>
The volume size, in gibibytes \(GiB\)\. This can be a number from 1 \- 1024\. If the volume type is EBS\-optimized, the minimum value is 10\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-elasticmapreduce-cluster-volumespecification-volumetype"></a>
The volume type\. Volume types supported are gp2, io1, standard sc1, st1 and gp3\. For gp3, customer will be able to configure IOPs but not throughput\. Throughput will default to 125 MiB/s\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)