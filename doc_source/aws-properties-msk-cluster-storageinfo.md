# AWS::MSK::Cluster StorageInfo<a name="aws-properties-msk-cluster-storageinfo"></a>

Contains information about storage volumes attached to MSK broker nodes\.

## Syntax<a name="aws-properties-msk-cluster-storageinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-storageinfo-syntax.json"></a>

```
{
  "[EBSStorageInfo](#cfn-msk-cluster-storageinfo-ebsstorageinfo)" : EBSStorageInfo
}
```

### YAML<a name="aws-properties-msk-cluster-storageinfo-syntax.yaml"></a>

```
  [EBSStorageInfo](#cfn-msk-cluster-storageinfo-ebsstorageinfo): 
    EBSStorageInfo
```

## Properties<a name="aws-properties-msk-cluster-storageinfo-properties"></a>

`EBSStorageInfo`  <a name="cfn-msk-cluster-storageinfo-ebsstorageinfo"></a>
EBS volume information\.  
*Required*: No  
*Type*: [EBSStorageInfo](aws-properties-msk-cluster-ebsstorageinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)