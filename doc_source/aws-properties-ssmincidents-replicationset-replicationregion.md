# AWS::SSMIncidents::ReplicationSet ReplicationRegion<a name="aws-properties-ssmincidents-replicationset-replicationregion"></a>

The `ReplicationRegion` property type specifies the Region and KMS key to add to the replication set\.

## Syntax<a name="aws-properties-ssmincidents-replicationset-replicationregion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-replicationset-replicationregion-syntax.json"></a>

```
{
  "[RegionConfiguration](#cfn-ssmincidents-replicationset-replicationregion-regionconfiguration)" : RegionConfiguration,
  "[RegionName](#cfn-ssmincidents-replicationset-replicationregion-regionname)" : String
}
```

### YAML<a name="aws-properties-ssmincidents-replicationset-replicationregion-syntax.yaml"></a>

```
  [RegionConfiguration](#cfn-ssmincidents-replicationset-replicationregion-regionconfiguration): 
    RegionConfiguration
  [RegionName](#cfn-ssmincidents-replicationset-replicationregion-regionname): String
```

## Properties<a name="aws-properties-ssmincidents-replicationset-replicationregion-properties"></a>

`RegionConfiguration`  <a name="cfn-ssmincidents-replicationset-replicationregion-regionconfiguration"></a>
Specifies the Region configuration\.  
*Required*: No  
*Type*: [RegionConfiguration](aws-properties-ssmincidents-replicationset-regionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionName`  <a name="cfn-ssmincidents-replicationset-replicationregion-regionname"></a>
Specifies the region name to add to the replication set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)