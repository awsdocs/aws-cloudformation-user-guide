# AWS::OpsWorks::Volume<a name="aws-resource-opsworks-volume"></a>

The `AWS::OpsWorks::Volume` resource registers an Amazon Elastic Block Store \(Amazon EBS\) volume with an AWS OpsWorks stack\.

**Topics**
+ [Syntax](#aws-resource-opsworks-volume-syntax)
+ [Properties](#aws-resource-opsworks-volume-properties)
+ [Return Value](#aws-resource-opsworks-volume-returnvalues)
+ [Example](#aws-resource-opsworks-volume-examples)

## Syntax<a name="aws-resource-opsworks-volume-syntax"></a>

### JSON<a name="aws-resource-opsworks-volume-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::Volume",
  "Properties" : {
    "[Ec2VolumeId](#cfn-opsworks-volume-ec2volumeid)" : String,
    "[MountPoint](#cfn-opsworks-volume-mountpoint)" : String,
    "[Name](#cfn-opsworks-volume-name)" : String,
    "[StackId](#cfn-opsworks-volume-stackid)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-volume-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::Volume"
Properties:
  [Ec2VolumeId](#cfn-opsworks-volume-ec2volumeid): String
  [MountPoint](#cfn-opsworks-volume-mountpoint): String
  [Name](#cfn-opsworks-volume-name): String
  [StackId](#cfn-opsworks-volume-stackid): String
```

## Properties<a name="aws-resource-opsworks-volume-properties"></a>

`Ec2VolumeId`  <a name="cfn-opsworks-volume-ec2volumeid"></a>
The ID of the Amazon EBS volume to register with the AWS OpsWorks stack\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MountPoint`  <a name="cfn-opsworks-volume-mountpoint"></a>
The mount point for the Amazon EBS volume, such as `/mnt/disk1`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-opsworks-volume-name"></a>
A name for the Amazon EBS volume\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StackId`  <a name="cfn-opsworks-volume-stackid"></a>
The ID of the AWS OpsWorks stack that AWS OpsWorks registers the volume to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-opsworks-volume-returnvalues"></a>

### Ref<a name="w3ab2c21c10d943c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the AWS OpsWorks volume ID, such as `1ab23cd4-92ff-4501-b37c-example`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-opsworks-volume-examples"></a>

The following example registers the `ec2volume` volume with the `opsworksstack` stack, both of which are declared elsewhere in the same template\.

### JSON<a name="aws-resource-opsworks-volume-example.json"></a>

```
"opsworksVolume": {
  "Type": "AWS::OpsWorks::Volume",
  "Properties": {
    "Ec2VolumeId": { "Ref": "ec2volume" },
    "MountPoint": "/dev/sdb",
    "Name": "testOpsWorksVolume",
    "StackId": { "Ref": "opsworksstack" }
  }
}
```

### YAML<a name="aws-resource-opsworks-volume-example.yaml"></a>

```
opsworksVolume:
  Type: AWS::OpsWorks::Volume
  Properties:
    Ec2VolumeId: !Ref 'ec2volume'
    MountPoint: /dev/sdb
    Name: testOpsWorksVolume
    StackId: !Ref 'opsworksstack'
```