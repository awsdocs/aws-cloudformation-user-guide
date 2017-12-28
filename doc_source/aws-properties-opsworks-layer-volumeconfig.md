# AWS OpsWorks VolumeConfiguration Type<a name="aws-properties-opsworks-layer-volumeconfig"></a>

Describes the Amazon EBS volumes for the [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type\.

## Syntax<a name="w3ab2c21c14e1407b5"></a>

### JSON<a name="aws-properties-opsworks-layer-volumeconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-iops)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-mountpoint)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-numberofdisks)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-raidlevel)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-size)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-volumetype)" : String
}
```

### YAML<a name="aws-properties-opsworks-layer-volumeconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-iops): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-mountpoint): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-numberofdisks): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-raidlevel): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-size): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-volconfig-volumetype): String
```

## Properties<a name="w3ab2c21c14e1407b7"></a>

`Iops`  
The number of I/O operations per second \(IOPS\) to provision for the volume\.  
*Required: *Conditional\. If you specify `io1` for the volume type, you must specify this property\.  
*Type*: Integer

`MountPoint`  
The volume mount point, such as `/dev/sdh`\.  
*Required: *Yes  
*Type*: String

`NumberOfDisks`  
The number of disks in the volume\.  
*Required: *Yes  
*Type*: Integer

`RaidLevel`  
The volume RAID level\.  
*Required: *No  
*Type*: Integer

`Size`  
The volume size\.  
*Required: *Yes  
*Type*: Integer

`VolumeType`  
The type of volume, such as magnetic or SSD\. For valid values, see [VolumeConfiguration](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_VolumeConfiguration.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *No  
*Type*: String