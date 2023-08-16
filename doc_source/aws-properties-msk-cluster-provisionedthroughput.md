# AWS::MSK::Cluster ProvisionedThroughput<a name="aws-properties-msk-cluster-provisionedthroughput"></a>

Contains information about provisioned throughput for EBS storage volumes attached to kafka broker nodes\.

## Syntax<a name="aws-properties-msk-cluster-provisionedthroughput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-provisionedthroughput-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-cluster-provisionedthroughput-enabled)" : Boolean,
  "[VolumeThroughput](#cfn-msk-cluster-provisionedthroughput-volumethroughput)" : Integer
}
```

### YAML<a name="aws-properties-msk-cluster-provisionedthroughput-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-cluster-provisionedthroughput-enabled): Boolean
  [VolumeThroughput](#cfn-msk-cluster-provisionedthroughput-volumethroughput): Integer
```

## Properties<a name="aws-properties-msk-cluster-provisionedthroughput-properties"></a>

`Enabled`  <a name="cfn-msk-cluster-provisionedthroughput-enabled"></a>
Provisioned throughput is enabled or not\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeThroughput`  <a name="cfn-msk-cluster-provisionedthroughput-volumethroughput"></a>
Throughput value of the EBS volumes for the data drive on each kafka broker node in MiB per second\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)