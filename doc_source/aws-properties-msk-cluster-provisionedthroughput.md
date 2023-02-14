# AWS::MSK::Cluster ProvisionedThroughput<a name="aws-properties-msk-cluster-provisionedthroughput"></a>

Specifies whether provisioned throughput is turned on and the volume throughput target\.

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
Specifies whether provisioned throughput is turned on for the cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeThroughput`  <a name="cfn-msk-cluster-provisionedthroughput-volumethroughput"></a>
The provisioned throughput rate in MiB per second\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)