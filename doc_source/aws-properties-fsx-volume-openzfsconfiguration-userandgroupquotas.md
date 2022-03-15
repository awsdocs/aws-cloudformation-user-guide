# AWS::FSx::Volume UserAndGroupQuotas<a name="aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas"></a>

An object specifying how much storage users or groups can use on the volume\.

## Syntax<a name="aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas-syntax.json"></a>

```
{
  "[Id](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-id)" : Integer,
  "[StorageCapacityQuotaGiB](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-storagecapacityquotagib)" : Integer,
  "[Type](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-type)" : String
}
```

### YAML<a name="aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas-syntax.yaml"></a>

```
  [Id](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-id): Integer
  [StorageCapacityQuotaGiB](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-storagecapacityquotagib): Integer
  [Type](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-type): String
```

## Properties<a name="aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas-properties"></a>

`Id`  <a name="cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-id"></a>
The ID of the user or group\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCapacityQuotaGiB`  <a name="cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-storagecapacityquotagib"></a>
The amount of storage that the user or group can use in gibibytes \(GiB\)\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-fsx-volume-openzfsconfiguration-userandgroupquotas-type"></a>
A value that specifies whether the quota applies to a user or group\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GROUP | USER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)