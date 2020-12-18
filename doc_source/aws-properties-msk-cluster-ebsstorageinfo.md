# AWS::MSK::Cluster EBSStorageInfo<a name="aws-properties-msk-cluster-ebsstorageinfo"></a>

Contains information about the EBS storage volumes attached to brokers\.

## Syntax<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax.json"></a>

```
{
  "[VolumeSize](#cfn-msk-cluster-ebsstorageinfo-volumesize)" : Integer
}
```

### YAML<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax.yaml"></a>

```
  [VolumeSize](#cfn-msk-cluster-ebsstorageinfo-volumesize): Integer
```

## Properties<a name="aws-properties-msk-cluster-ebsstorageinfo-properties"></a>

`VolumeSize`  <a name="cfn-msk-cluster-ebsstorageinfo-volumesize"></a>
The size in GiB of the EBS volume for the data drive on each broker node\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)