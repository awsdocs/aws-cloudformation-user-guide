# Amazon EMR Cluster InstanceFleetConfig<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig"></a>

The `InstanceFleetConfig` property type specifies a Spot instance fleet configuration for the cluster\. For more information, see [Configure Instance Fleets](http://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html) in the *Amazon EMR Management Guide*\. `InstanceFleetConfig` is the property type for the `CoreInstanceFleet` and `MasterInstanceFleet` subproperties of the [Amazon EMR Cluster JobFlowInstancesConfig](aws-properties-emr-cluster-jobflowinstancesconfig.md) property type\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="w3ab2c21c14e1081b7"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-syntax.json"></a>

```
{
  "[InstanceTypeConfigs](#cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs)" : [ [*InstanceTypeConfig*](aws-properties-elasticmapreduce-cluster-instancetypeconfig.md) ],
  "[LaunchSpecifications](#cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications)" : [*InstanceFleetProvisioningSpecifications*](aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications.md),
  "[Name](#cfn-elasticmapreduce-cluster-instancefleetconfig-name)" : String,
  "[TargetOnDemandCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity)" : Integer,
  "[TargetSpotCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-syntax.yaml"></a>

```
[InstanceTypeConfigs](#cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs): 
  - [*InstanceTypeConfig*](aws-properties-elasticmapreduce-cluster-instancetypeconfig.md)
[LaunchSpecifications](#cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications):
  [*InstanceFleetProvisioningSpecifications*](aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications.md)
[Name](#cfn-elasticmapreduce-cluster-instancefleetconfig-name): String
[TargetOnDemandCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity): Integer
[TargetSpotCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity): Integer
```

## Properties<a name="w3ab2c21c14e1081b9"></a>

`InstanceTypeConfigs`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs"></a>
The instance type configurations that define the EC2 instances in the instance fleet\. Duplicates not allowed\.  
*Required*: No  
*Type*: List of [Amazon EMR Cluster InstanceTypeConfig](aws-properties-elasticmapreduce-cluster-instancetypeconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchSpecifications`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications"></a>
The launch specification for the instance fleet\.  
*Required*: No  
*Type*: [Amazon EMR Cluster InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-name"></a>
The friendly name of the instance fleet\. For constraints, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TargetOnDemandCapacity`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity"></a>
The target capacity of On\-Demand units for the instance fleet, which determines how many On\-Demand instances to provision\. For more information, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetSpotCapacity`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity"></a>
The target capacity of Spot units for the instance fleet, which determines how many Spot instances to provision\. For more information, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)