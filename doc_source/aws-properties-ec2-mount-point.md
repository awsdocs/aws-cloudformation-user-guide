# EC2 MountPoint Property Type<a name="aws-properties-ec2-mount-point"></a>

The EC2 MountPoint property is an embedded property of the AWS::EC2::Instance type\.

## Syntax<a name="w3ab2c21c14d571b5"></a>

### JSON<a name="aws-properties-ec2-mount-point-syntax.json"></a>

```
{
  "Device" : String,
  "VolumeId" : String
}
```

### YAML<a name="aws-properties-ec2-mount-point-syntax.yaml"></a>

```
Device: String,
VolumeId: String
```

## Properties<a name="w3ab2c21c14d571b7"></a>

`Device`  
How the device is exposed to the instance \(such as /dev/sdh, or xvdh\)\.  
*Required: *Yes  
*Type*: String

`VolumeId`  
The ID of the Amazon EBS volume\. The volume and instance must be within the same Availability Zone and the instance must be running\.  
*Required: *Yes  
*Type*: String

## Example<a name="w3ab2c21c14d571b9"></a>

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

## See Also<a name="w3ab2c21c14d571c11"></a>

+ 

+ 