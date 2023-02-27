# AWS::OpenSearchService::Domain EBSOptions<a name="aws-properties-opensearchservice-domain-ebsoptions"></a>

The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the OpenSearch Service domain\. For more information, see [EBS volume size limits](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/limits.html#ebsresource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-opensearchservice-domain-ebsoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-ebsoptions-syntax.json"></a>

```
{
  "[EBSEnabled](#cfn-opensearchservice-domain-ebsoptions-ebsenabled)" : Boolean,
  "[Iops](#cfn-opensearchservice-domain-ebsoptions-iops)" : Integer,
  "[Throughput](#cfn-opensearchservice-domain-ebsoptions-throughput)" : Integer,
  "[VolumeSize](#cfn-opensearchservice-domain-ebsoptions-volumesize)" : Integer,
  "[VolumeType](#cfn-opensearchservice-domain-ebsoptions-volumetype)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-ebsoptions-syntax.yaml"></a>

```
  [EBSEnabled](#cfn-opensearchservice-domain-ebsoptions-ebsenabled): Boolean
  [Iops](#cfn-opensearchservice-domain-ebsoptions-iops): Integer
  [Throughput](#cfn-opensearchservice-domain-ebsoptions-throughput): Integer
  [VolumeSize](#cfn-opensearchservice-domain-ebsoptions-volumesize): Integer
  [VolumeType](#cfn-opensearchservice-domain-ebsoptions-volumetype): String
```

## Properties<a name="aws-properties-opensearchservice-domain-ebsoptions-properties"></a>

`EBSEnabled`  <a name="cfn-opensearchservice-domain-ebsoptions-ebsenabled"></a>
Specifies whether Amazon EBS volumes are attached to data nodes in the OpenSearch Service domain\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-opensearchservice-domain-ebsoptions-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. This property applies only to the `gp3` and provisioned IOPS EBS volume types\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throughput`  <a name="cfn-opensearchservice-domain-ebsoptions-throughput"></a>
The throughput \(in MiB/s\) of the EBS volumes attached to data nodes\. Applies only to the `gp3` volume type\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-opensearchservice-domain-ebsoptions-volumesize"></a>
The size \(in GiB\) of the EBS volume for each data node\. The minimum and maximum size of an EBS volume depends on the EBS volume type and the instance type to which it is attached\. For more information, see [EBS volume size limits](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/limits.html#ebsresource) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-opensearchservice-domain-ebsoptions-volumetype"></a>
The EBS volume type to use with the OpenSearch Service domain\. If you choose `gp3`, you must also specify values for `Iops` and `Throughput`\. For more information about each type, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | gp3 | io1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)