# AWS::MSK::Cluster EBSStorageInfo<a name="aws-properties-msk-cluster-ebsstorageinfo"></a>

Contains information about the EBS storage volumes attached to brokers\.

## Syntax<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax.json"></a>

```
{
  "[ProvisionedThroughput](#cfn-msk-cluster-ebsstorageinfo-provisionedthroughput)" : ProvisionedThroughput,
  "[VolumeSize](#cfn-msk-cluster-ebsstorageinfo-volumesize)" : Integer
}
```

### YAML<a name="aws-properties-msk-cluster-ebsstorageinfo-syntax.yaml"></a>

```
  [ProvisionedThroughput](#cfn-msk-cluster-ebsstorageinfo-provisionedthroughput): 
    ProvisionedThroughput
  [VolumeSize](#cfn-msk-cluster-ebsstorageinfo-volumesize): Integer
```

## Properties<a name="aws-properties-msk-cluster-ebsstorageinfo-properties"></a>

`ProvisionedThroughput`  <a name="cfn-msk-cluster-ebsstorageinfo-provisionedthroughput"></a>
Specifies whether provisioned throughput is turned on and the volume throughput target\.  
*Required*: No  
*Type*: [ProvisionedThroughput](aws-properties-msk-cluster-provisionedthroughput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-msk-cluster-ebsstorageinfo-volumesize"></a>
The size in GiB of the EBS volume for the data drive on each broker node\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)