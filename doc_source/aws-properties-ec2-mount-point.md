# EC2 MountPoint Property Type<a name="aws-properties-ec2-mount-point"></a>

The EC2 MountPoint property is an embedded property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) type\.

## Syntax<a name="w3ab2c21c14d731b5"></a>

### JSON<a name="aws-properties-ec2-mount-point-syntax.json"></a>

```
{
  "[Device](#cfn-ec2-mountpoint-device)" : String,
  "[VolumeId](#cfn-ec2-mountpoint-volumeid)" : String
}
```

### YAML<a name="aws-properties-ec2-mount-point-syntax.yaml"></a>

```
[Device](#cfn-ec2-mountpoint-device): String,
[VolumeId](#cfn-ec2-mountpoint-volumeid): String
```

## Properties<a name="w3ab2c21c14d731b7"></a>

`Device`  <a name="cfn-ec2-mountpoint-device"></a>
How the device is exposed to the instance \(such as /dev/sdh, or xvdh\)\.  
*Required*: Yes  
*Type*: String

`VolumeId`  <a name="cfn-ec2-mountpoint-volumeid"></a>
The ID of the Amazon EBS volume\. The volume and instance must be within the same Availability Zone and the instance must be running\.  
*Required*: Yes  
*Type*: String

## Example<a name="w3ab2c21c14d731b9"></a>

This mount point \(specified in the `Volumes` property in the EC2 instance\) refers to a named EBS volume, "NewVolume"\.

```
"Ec2Instance" : {
   "Type" : "AWS::EC2::Instance",
   "Properties" : {
      "AvailabilityZone" : {
         "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "TestAz" ]
      },
      "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
      "KeyName" : { "Ref" : "KeyName" },
      "ImageId" : {
         "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]
      },
      "Volumes" : [
         { "VolumeId" : { "Ref" : "NewVolume" }, "Device" : "/dev/sdk" }
      ]
   }
},
"NewVolume" : {
   "Type" : "AWS::EC2::Volume",
   "Properties" : {
      "Size" : "100",
      "AvailabilityZone" : {
         "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "TestAz" ]
      }
   }
}
```

## See Also<a name="w3ab2c21c14d731c11"></a>
+ [AWS::EC2::Instance](aws-properties-ec2-instance.md)
+ [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md)