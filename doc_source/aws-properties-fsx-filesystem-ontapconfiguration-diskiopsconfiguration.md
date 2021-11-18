# AWS::FSx::FileSystem DiskIopsConfiguration<a name="aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration"></a>

The SSD IOPS \(input/output operations per second\) configuration for an Amazon FSx for NetApp ONTAP file system\. The default is 3 IOPS per GB of storage capacity, but you can provision additional IOPS per GB of storage\. The configuration consists of the total number of provisioned SSD IOPS and how the amount was provisioned \(by the customer or by the system\)\.

## Syntax<a name="aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-syntax.json"></a>

```
{
  "[Iops](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-iops)" : Integer,
  "[Mode](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-mode)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-syntax.yaml"></a>

```
  [Iops](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-iops): Integer
  [Mode](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-mode): String
```

## Properties<a name="aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-properties"></a>

`Iops`  <a name="cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-iops"></a>
The total number of SSD IOPS provisioned for the file system\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration-mode"></a>
Specifies whether the number of IOPS for the file system is using the system default \(`AUTOMATIC`\) or was provisioned by the customer \(`USER_PROVISIONED`\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | USER_PROVISIONED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)