# AWS::Elasticsearch::Domain EBSOptions<a name="aws-properties-elasticsearch-domain-ebsoptions"></a>

The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the OpenSearch Service domain\. For more information, see [EBS volume size limits](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/limits.html#ebsresource) in the *Amazon OpenSearch Service Developer Guide*\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-ebsoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-ebsoptions-syntax.json"></a>

```
{
  "[EBSEnabled](#cfn-elasticsearch-domain-ebsoptions-ebsenabled)" : Boolean,
  "[Iops](#cfn-elasticsearch-domain-ebsoptions-iops)" : Integer,
  "[VolumeSize](#cfn-elasticsearch-domain-ebsoptions-volumesize)" : Integer,
  "[VolumeType](#cfn-elasticsearch-domain-ebsoptions-volumetype)" : String
}
```

### YAML<a name="aws-properties-elasticsearch-domain-ebsoptions-syntax.yaml"></a>

```
  [EBSEnabled](#cfn-elasticsearch-domain-ebsoptions-ebsenabled): Boolean
  [Iops](#cfn-elasticsearch-domain-ebsoptions-iops): Integer
  [VolumeSize](#cfn-elasticsearch-domain-ebsoptions-volumesize): Integer
  [VolumeType](#cfn-elasticsearch-domain-ebsoptions-volumetype): String
```

## Properties<a name="aws-properties-elasticsearch-domain-ebsoptions-properties"></a>

`EBSEnabled`  <a name="cfn-elasticsearch-domain-ebsoptions-ebsenabled"></a>
Specifies whether Amazon EBS volumes are attached to data nodes in the OpenSearch Service domain\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-elasticsearch-domain-ebsoptions-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. This property applies only to provisioned IOPS EBS volume types\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-elasticsearch-domain-ebsoptions-volumesize"></a>
The size \(in GiB\) of the EBS volume for each data node\. The minimum and maximum size of an EBS volume depends on the EBS volume type and the instance type to which it is attached\. For more information, see [EBS volume size limits](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/limits.html#ebsresource) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-elasticsearch-domain-ebsoptions-volumetype"></a>
The EBS volume type to use with the OpenSearch Service domain, such as standard, gp2, or io1\. For more information about each type, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)