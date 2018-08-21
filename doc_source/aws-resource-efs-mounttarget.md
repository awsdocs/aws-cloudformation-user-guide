# AWS::EFS::MountTarget<a name="aws-resource-efs-mounttarget"></a>

The `AWS::EFS::MountTarget` resource creates a mount target for an Amazon Elastic File System \(Amazon EFS\) file system \([AWS::EFS::FileSystem](aws-resource-efs-filesystem.md)\)\. Use the mount target to mount file systems on Amazon Elastic Compute Cloud \(Amazon EC2\) instances\.

For more information on creating a mount target for a file system, see [CreateMountTarget](http://docs.aws.amazon.com/efs/latest/ug/API_CreateMountTarget.html) in the *Amazon Elastic File System User Guide*\. For a detailed overview of deploying EC2 instances associated with an Amazon EFS file system, see [Amazon Elastic File System Sample Template](quickref-efs.md)\.

**Note**  
EC2 instances and the mount target that they connect to must be in a VPC with DNS enabled\.

**Topics**
+ [Syntax](#aws-resource-efs-mounttarget-syntax)
+ [Properties](#w3ab2c21c10d575c13)
+ [Return Values](#w3ab2c21c10d575c15)
+ [Template Example](#w3ab2c21c10d575c17)
+ [Additional Resources](#w3ab2c21c10d575c19)

## Syntax<a name="aws-resource-efs-mounttarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-mounttarget-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::MountTarget",
  "Properties" : {
    "[FileSystemId](#cfn-efs-mounttarget-filesystemid)" : String,
    "[IpAddress](#cfn-efs-mounttarget-ipaddress)" : String,
    "[SecurityGroups](#cfn-efs-mounttarget-securitygroups)" : [ String, ... ],
    "[SubnetId](#cfn-efs-mounttarget-subnetid)" : String
  }
}
```

### YAML<a name="aws-resource-efs-mounttarget-syntax.yaml"></a>

```
Type: "AWS::EFS::MountTarget"
Properties:
  [FileSystemId](#cfn-efs-mounttarget-filesystemid): String
  [IpAddress](#cfn-efs-mounttarget-ipaddress): String
  [SecurityGroups](#cfn-efs-mounttarget-securitygroups):
    [ String, ... ]
  [SubnetId](#cfn-efs-mounttarget-subnetid): String
```

## Properties<a name="w3ab2c21c10d575c13"></a>

`FileSystemId`  <a name="cfn-efs-mounttarget-filesystemid"></a>
The ID of the file system for which you want to create the mount target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
Before updating this property, stop EC2 instances that are using this mount target, and then restart them after the update is complete\. This allows the instances to unmount the file system before the mount target is replaced\. If you don't stop and restart them, instances or applications that are using those mounts might be disrupted when the mount target is deleted \(uncommitted writes might be lost\)\.

`IpAddress`  <a name="cfn-efs-mounttarget-ipaddress"></a>
An IPv4 address that is within the address range of the subnet that is specified in the `SubnetId` property\. If you don't specify an IP address, Amazon EFS automatically assigns an address that is within the range of the subnet\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
Before updating this property, stop EC2 instances that are using this mount target, and then restart them after the update is complete\. This allows the instances to unmount the file system before the mount target is replaced\. If you don't stop and restart them, instances or applications that are using those mounts might be disrupted when the mount target is deleted \(uncommitted writes might be lost\)\.

`SecurityGroups`  <a name="cfn-efs-mounttarget-securitygroups"></a>
A maximum of five VPC security group IDs that are in the same VPC as the subnet that is specified in the `SubnetId` property\. For more information about security groups and mount targets, see [Security](http://docs.aws.amazon.com/efs/latest/ug/security-considerations.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetId`  <a name="cfn-efs-mounttarget-subnetid"></a>
The ID of the subnet in which you want to add the mount target\.  
For each file system, you can create only one mount target per Availability Zone \(AZ\)\. All EC2 instances in an AZ share a single mount target for a file system\. If you create multiple mount targets for a single file system, do not specify a subnet that is an AZ that already has a mount target associated with the same file system\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
Before updating this property, stop EC2 instances that are using this mount target and then restart them after the update is complete\. That way the instances can unmount the file system before the mount target is replaced\. If you don't stop and restart them, instances or applications that are using those mounts might be disrupted when the mount target is deleted \(uncommitted writes might be lost\)\.

## Return Values<a name="w3ab2c21c10d575c15"></a>

### Ref<a name="w3ab2c21c10d575c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID, such as `fsmt-55a4413c`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Example<a name="w3ab2c21c10d575c17"></a>

The following example declares a mount target that is associated with a file system, subnet, and security group, which are all declared in the same template\. EC2 instances that are in the same AZ as the mount target can use the mount target to connect to the associated file system\. For information about mounting file systems on EC2 instances, see [Mounting File Systems](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html) in the *Amazon Elastic File System User Guide*\.

### JSON<a name="aws-resource-efs-mounttarget-example.json"></a>

```
"MountTarget": {
  "Type": "AWS::EFS::MountTarget",
  "Properties": {
    "FileSystemId": { "Ref": "FileSystem" },
    "SubnetId": { "Ref": "Subnet" },
    "SecurityGroups": [ { "Ref": "MountTargetSecurityGroup" } ]        
  }
}
```

### YAML<a name="aws-resource-efs-mounttarget-example.yaml"></a>

```
MountTarget: 
  Type: "AWS::EFS::MountTarget"
  Properties: 
    FileSystemId: 
      Ref: "FileSystem"
    SubnetId: 
      Ref: "Subnet"
    SecurityGroups: 
      - 
        Ref: "MountTargetSecurityGroup"
```

## Additional Resources<a name="w3ab2c21c10d575c19"></a>

For a complete sample template, see [Amazon Elastic File System Sample Template](quickref-efs.md)\.