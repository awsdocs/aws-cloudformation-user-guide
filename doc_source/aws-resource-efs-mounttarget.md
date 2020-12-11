# AWS::EFS::MountTarget<a name="aws-resource-efs-mounttarget"></a>

The `AWS::EFS::MountTarget` resource is an Amazon EFS resource that creates a mount target for an EFS file system\. You can then mount the file system on Amazon EC2 instances or other resources by using the mount target\.

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
Type: AWS::EFS::MountTarget
Properties: 
  [FileSystemId](#cfn-efs-mounttarget-filesystemid): String
  [IpAddress](#cfn-efs-mounttarget-ipaddress): String
  [SecurityGroups](#cfn-efs-mounttarget-securitygroups): 
    - String
  [SubnetId](#cfn-efs-mounttarget-subnetid): String
```

## Properties<a name="aws-resource-efs-mounttarget-properties"></a>

`FileSystemId`  <a name="cfn-efs-mounttarget-filesystemid"></a>
The ID of the file system for which to create the mount target\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^(arn:aws[-a-z]*:elasticfilesystem:[0-9a-z-:]+:file-system/fs-[0-9a-f]{8,40}|fs-[0-9a-f]{8,40})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddress`  <a name="cfn-efs-mounttarget-ipaddress"></a>
Valid IPv4 address within the address range of the specified subnet\.  
*Required*: No  
*Type*: String  
*Minimum*: `7`  
*Maximum*: `15`  
*Pattern*: `^[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-efs-mounttarget-securitygroups"></a>
Up to five VPC security group IDs, of the form `sg-xxxxxxxx`\. These must be for the same VPC as subnet specified\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-efs-mounttarget-subnetid"></a>
The ID of the subnet to add the mount target in\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `15`  
*Maximum*: `47`  
*Pattern*: `^subnet-[0-9a-f]{8,40}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-efs-mounttarget-return-values"></a>

### Ref<a name="aws-resource-efs-mounttarget-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For example: 

 `{"Ref":"fsmt-12345678"}`\.

For the Amazon EFS file system mount target `fsmt-12345678`, Ref returns the mount target ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-efs-mounttarget-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-efs-mounttarget-return-values-fn--getatt-fn--getatt"></a>

`IpAddress`  <a name="IpAddress-fn::getatt"></a>
The IPv4 address of the mount target\.

## Examples<a name="aws-resource-efs-mounttarget--examples"></a>



### Declare a Mount Target for an EFS File System<a name="aws-resource-efs-mounttarget--examples--Declare_a_Mount_Target_for_an_EFS_File_System"></a>

The following example declares a mount target that is associated with a file system, subnet, and security group, which are all declared in the same template\. EC2 instances that are in the same Availability Zone \(AZ\) as the mount target can use the mount target to connect to the associated file system\. For information about mounting file systems on EC2 instances, see [Mounting File Systems](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html) in the *EFS User Guide*\.

#### JSON<a name="aws-resource-efs-mounttarget--examples--Declare_a_Mount_Target_for_an_EFS_File_System--json"></a>

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

#### YAML<a name="aws-resource-efs-mounttarget--examples--Declare_a_Mount_Target_for_an_EFS_File_System--yaml"></a>

```
MountTarget: 
  Type: AWS::EFS::MountTarget
  Properties: 
    FileSystemId: 
      Ref: "FileSystem"
    SubnetId: 
      Ref: "Subnet"
    SecurityGroups: 
      - Ref: "MountTargetSecurityGroup"
```

## See also<a name="aws-resource-efs-mounttarget--seealso"></a>
+  [Amazon EFS: How It Works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html) 
+  [Creating Mount Targets](https://docs.aws.amazon.com/efs/latest/ug/accessing-fs.html) 
+  [Walkthrough: Mounting a File System On\-Premises](https://docs.aws.amazon.com/efs/latest/ug/efs-onpremises.html) 

