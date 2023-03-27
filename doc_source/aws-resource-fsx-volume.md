# AWS::FSx::Volume<a name="aws-resource-fsx-volume"></a>

Creates an FSx for ONTAP or Amazon FSx for OpenZFS storage volume\.

## Syntax<a name="aws-resource-fsx-volume-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-volume-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::Volume",
  "Properties" : {
      "[BackupId](#cfn-fsx-volume-backupid)" : String,
      "[Name](#cfn-fsx-volume-name)" : String,
      "[OntapConfiguration](#cfn-fsx-volume-ontapconfiguration)" : OntapConfiguration,
      "[OpenZFSConfiguration](#cfn-fsx-volume-openzfsconfiguration)" : OpenZFSConfiguration,
      "[Tags](#cfn-fsx-volume-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VolumeType](#cfn-fsx-volume-volumetype)" : String
    }
}
```

### YAML<a name="aws-resource-fsx-volume-syntax.yaml"></a>

```
Type: AWS::FSx::Volume
Properties: 
  [BackupId](#cfn-fsx-volume-backupid): String
  [Name](#cfn-fsx-volume-name): String
  [OntapConfiguration](#cfn-fsx-volume-ontapconfiguration): 
    OntapConfiguration
  [OpenZFSConfiguration](#cfn-fsx-volume-openzfsconfiguration): 
    OpenZFSConfiguration
  [Tags](#cfn-fsx-volume-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VolumeType](#cfn-fsx-volume-volumetype): String
```

## Properties<a name="aws-resource-fsx-volume-properties"></a>

`BackupId`  <a name="cfn-fsx-volume-backupid"></a>
Specifies the ID of the volume backup to use to create a new volume\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-fsx-volume-name"></a>
The name of the volume\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `203`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,203}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OntapConfiguration`  <a name="cfn-fsx-volume-ontapconfiguration"></a>
The configuration of an Amazon FSx for NetApp ONTAP volume\.  
*Required*: No  
*Type*: [OntapConfiguration](aws-properties-fsx-volume-ontapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenZFSConfiguration`  <a name="cfn-fsx-volume-openzfsconfiguration"></a>
The configuration of an Amazon FSx for OpenZFS volume\.  
*Required*: No  
*Type*: [OpenZFSConfiguration](aws-properties-fsx-volume-openzfsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fsx-volume-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-fsx-volume-volumetype"></a>
The type of the volume\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ONTAP | OPENZFS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-fsx-volume-return-values"></a>

### Ref<a name="aws-resource-fsx-volume-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID for the volume\. For example:

`{"Ref":"vol_logical_id"}`

Returns `fsvol-0123456789abcdef6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-volume-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-volume-return-values-fn--getatt-fn--getatt"></a>

`ResourceARN`  <a name="ResourceARN-fn::getatt"></a>
Returns the volume's Amazon Resource Name \(ARN\)\.  
Example: `arn:aws:fsx:us-east-2:111122223333:volume/fs-0123456789abcdef9/fsvol-01234567891112223`

`UUID`  <a name="UUID-fn::getatt"></a>
Returns the volume's universally unique identifier \(UUID\)\.  
Example: `abcd0123-cd45-ef67-11aa-1111aaaa23bc`

`VolumeId`  <a name="VolumeId-fn::getatt"></a>
Returns the volume's ID\.  
Example: `fsvol-0123456789abcdefa`

## Examples<a name="aws-resource-fsx-volume--examples"></a>

### Create an ONTAP volume<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume"></a>

#### JSON<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume--json"></a>

```
{
  "OntapVolumeWithAllConfigs": {
    "Type": "AWS::FSx::Volume",
    "Properties": {
      "Name": "volume1",
      "OntapConfiguration": {
        "JunctionPath": "/volume1",
        "SecurityStyle": "MIXED",
        "SizeInMegabytes": 40,
        "StorageEfficiencyEnabled": true,
        "StorageVirtualMachineId": {
          "Ref": "OntapStorageVirtualMachineWithAllConfigs"
        },
        "TieringPolicy": {
          "CoolingPeriod": 41,
          "Name": "AUTO"
        }
      },
      "Tags": [
        {
          "Key": "Name",
          "Value": "OntapVolume"
        }
      ],
      "VolumeType": "ONTAP"
    }
  }
}
```

#### YAML<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume--yaml"></a>

```
OntapVolumeWithAllConfigs:
  Type: 'AWS::FSx::Volume'
  Properties:
    Name: volume1
    OntapConfiguration:
      JunctionPath: /volume1
      SecurityStyle: MIXED
      SizeInMegabytes: 40
      StorageEfficiencyEnabled: true
      StorageVirtualMachineId: !Ref OntapStorageVirtualMachineWithAllConfigs
      TieringPolicy:
        CoolingPeriod: 41
        Name: AUTO
    Tags:
      - Key: Name
        Value: OntapVolume
    VolumeType: ONTAP
```

### Create an ONTAP volume from a backup<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume_from_a_backup"></a>

This example creates a volume from an existing backup: `backup-0123abc456defghij`

#### JSON<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume_from_a_backup--json"></a>

```
{
  "OntapVolumeFromBackupWithAllConfigs": {
    "Type": "AWS::FSx::Volume",
    "Properties": {
    "BackupId": "backup-0123abc456defghij",
      "Name": "volume11",
      "OntapConfiguration": {
        "JunctionPath": "/volume11",
        "SecurityStyle": "UNIX",
        "SizeInMegabytes": 41,
        "StorageEfficiencyEnabled": true,
        "StorageVirtualMachineId": {
          "Ref": "StorageVirtualMachineWithAllConfigs"
        },
        "TieringPolicy": {
          "CoolingPeriod": 42,
          "Name": "AUTO"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-fsx-volume--examples--Create_an_ONTAP_volume_from_a_backup--yaml"></a>

```
OntapVolumeFromBackupWithAllConfigs:
  Type: "AWS::FSx::Volume"
  Properties:
  BackupId: "backup-0123abc456defghij"
    Name: "volume11"
    OntapConfiguration:
      JunctionPath: "/volume11"
      SecurityStyle: "UNIX"
      SizeInMegabytes: 41
      StorageEfficiencyEnabled: True
      StorageVirtualMachineId: !Ref StorageVirtualMachineWithAllConfigs
      TieringPolicy:
        CoolingPeriod: 42
        Name: "AUTO"
```