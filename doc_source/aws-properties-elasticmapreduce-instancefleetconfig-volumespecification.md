# Amazon EMR InstanceFleetConfig VolumeSpecification<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification"></a>

Use the `VolumeSpecification` property to specify settings—such as volume type, IOPS, and size \(GiB\)—for the Amazon EBS volume attached to an EC2 instance in the fleet\. `VolumeSpecification` is a subproperty of the [Amazon EMR InstanceFleetConfig EbsBlockDeviceConfig](aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig.md) property\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-iops)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-sizeingb)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-iops): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-sizeingb): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-volumetype): String
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-properties"></a>

`Iops`  
The number of I/O operations per second \(IOPS\) that the volume supports\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Replacement

`SizeInGB`  
The volume size, in gibibytes \(GiB\)\. For valid values, see [VolumeSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: Replacement

`VolumeType`  
The volume type\. For valid values, see [VolumeSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement