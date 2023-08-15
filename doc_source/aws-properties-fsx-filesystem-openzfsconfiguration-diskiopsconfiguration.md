# AWS::FSx::FileSystem DiskIopsConfiguration<a name="aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration"></a>

The SSD IOPS \(input/output operations per second\) configuration for an Amazon FSx for NetApp ONTAP, Amazon FSx for Windows File Server, or FSx for OpenZFS file system\. By default, Amazon FSx automatically provisions 3 IOPS per GB of storage capacity\. You can provision additional IOPS per GB of storage\. The configuration consists of the total number of provisioned SSD IOPS and how it is was provisioned, or the mode \(by the customer or by Amazon FSx\)\.

## Syntax<a name="aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-syntax.json"></a>

```
{
  "[Iops](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-iops)" : Integer,
  "[Mode](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-mode)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-syntax.yaml"></a>

```
  [Iops](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-iops): Integer
  [Mode](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-mode): String
```

## Properties<a name="aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-properties"></a>

`Iops`  <a name="cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-iops"></a>
The total number of SSD IOPS provisioned for the file system\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration-mode"></a>
Specifies whether the file system is using the `AUTOMATIC` setting of SSD IOPS of 3 IOPS per GB of storage capacity, , or if it using a `USER_PROVISIONED` value\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | USER_PROVISIONED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)