# AWS::Elasticsearch::Domain EBSOptions<a name="aws-properties-elasticsearch-domain-ebsoptions"></a>

The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the Amazon ES domain\. For more information, see [Configuring EBS\-based Storage](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-ebs) in the *Amazon Elasticsearch Service Developer Guide*\.

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
Specifies whether Amazon EBS volumes are attached to data nodes in the Amazon ES domain\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-elasticsearch-domain-ebsoptions-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. This property applies only to the Provisioned IOPS \(SSD\) EBS volume type\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-elasticsearch-domain-ebsoptions-volumesize"></a>
The size \(in GiB\) of the EBS volume for each data node\. The minimum and maximum size of an EBS volume depends on the EBS volume type and the instance type to which it is attached\. For more information, see [Configuring EBS\-based Storage](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-ebs) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-elasticsearch-domain-ebsoptions-volumetype"></a>
The EBS volume type to use with the Amazon ES domain, such as standard, gp2, or io1\. For more information about each type, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)