# AWS::MSK::Cluster StorageInfo<a name="aws-properties-msk-cluster-storageinfo"></a>

Contains information about storage volumes attached to MSK broker nodes\.

## Syntax<a name="aws-properties-msk-cluster-storageinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-storageinfo-syntax.json"></a>

```
{
  "[EBSStorageInfo](#cfn-msk-cluster-storageinfo-ebsstorageinfo)" : [EBSStorageInfo](aws-properties-msk-cluster-ebsstorageinfo.md)
}
```

### YAML<a name="aws-properties-msk-cluster-storageinfo-syntax.yaml"></a>

```
  [EBSStorageInfo](#cfn-msk-cluster-storageinfo-ebsstorageinfo): 
    [EBSStorageInfo](aws-properties-msk-cluster-ebsstorageinfo.md)
```

## Properties<a name="aws-properties-msk-cluster-storageinfo-properties"></a>

`EBSStorageInfo`  <a name="cfn-msk-cluster-storageinfo-ebsstorageinfo"></a>
EBS volume information\.  
*Required*: No  
*Type*: [EBSStorageInfo](aws-properties-msk-cluster-ebsstorageinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-2`
