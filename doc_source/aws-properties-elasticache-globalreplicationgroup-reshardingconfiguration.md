# AWS::ElastiCache::GlobalReplicationGroup ReshardingConfiguration<a name="aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration"></a>

A list of `PreferredAvailabilityZones` objects that specifies the configuration of a node group in the resharded cluster\.

## Syntax<a name="aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration-syntax.json"></a>

```
{
  "[NodeGroupId](#cfn-elasticache-globalreplicationgroup-reshardingconfiguration-nodegroupid)" : String,
  "[PreferredAvailabilityZones](#cfn-elasticache-globalreplicationgroup-reshardingconfiguration-preferredavailabilityzones)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration-syntax.yaml"></a>

```
  [NodeGroupId](#cfn-elasticache-globalreplicationgroup-reshardingconfiguration-nodegroupid): String
  [PreferredAvailabilityZones](#cfn-elasticache-globalreplicationgroup-reshardingconfiguration-preferredavailabilityzones): 
    - String
```

## Properties<a name="aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration-properties"></a>

`NodeGroupId`  <a name="cfn-elasticache-globalreplicationgroup-reshardingconfiguration-nodegroupid"></a>
Either the ElastiCache for Redis supplied 4\-digit id or a user supplied id for the node group these configuration values apply to\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4`  
*Pattern*: `\d+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredAvailabilityZones`  <a name="cfn-elasticache-globalreplicationgroup-reshardingconfiguration-preferredavailabilityzones"></a>
A list of preferred availability zones for the nodes in this cluster\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)