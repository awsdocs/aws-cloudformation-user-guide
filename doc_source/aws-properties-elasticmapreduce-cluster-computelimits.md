# AWS::EMR::Cluster ComputeLimits<a name="aws-properties-elasticmapreduce-cluster-computelimits"></a>

 The EC2 unit limits for a managed scaling policy\. The managed scaling activity of a cluster can not be above or below these limits\. The limit only applies to the core and task nodes\. The master node cannot be scaled after initial configuration\. 

## Syntax<a name="aws-properties-elasticmapreduce-cluster-computelimits-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-computelimits-syntax.json"></a>

```
{
  "[MaximumCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumcapacityunits)" : Integer,
  "[MaximumCoreCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumcorecapacityunits)" : Integer,
  "[MaximumOnDemandCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumondemandcapacityunits)" : Integer,
  "[MinimumCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-minimumcapacityunits)" : Integer,
  "[UnitType](#cfn-elasticmapreduce-cluster-computelimits-unittype)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-computelimits-syntax.yaml"></a>

```
  [MaximumCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumcapacityunits): Integer
  [MaximumCoreCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumcorecapacityunits): Integer
  [MaximumOnDemandCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-maximumondemandcapacityunits): Integer
  [MinimumCapacityUnits](#cfn-elasticmapreduce-cluster-computelimits-minimumcapacityunits): Integer
  [UnitType](#cfn-elasticmapreduce-cluster-computelimits-unittype): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-computelimits-properties"></a>

`MaximumCapacityUnits`  <a name="cfn-elasticmapreduce-cluster-computelimits-maximumcapacityunits"></a>
 The upper boundary of EC2 units\. It is measured through vCPU cores or instances for instance groups and measured through units for instance fleets\. Managed scaling activities are not allowed beyond this boundary\. The limit only applies to the core and task nodes\. The master node cannot be scaled after initial configuration\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumCoreCapacityUnits`  <a name="cfn-elasticmapreduce-cluster-computelimits-maximumcorecapacityunits"></a>
 The upper boundary of EC2 units for core node type in a cluster\. It is measured through vCPU cores or instances for instance groups and measured through units for instance fleets\. The core units are not allowed to scale beyond this boundary\. The parameter is used to split capacity allocation between core and task nodes\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumOnDemandCapacityUnits`  <a name="cfn-elasticmapreduce-cluster-computelimits-maximumondemandcapacityunits"></a>
 The upper boundary of On\-Demand EC2 units\. It is measured through vCPU cores or instances for instance groups and measured through units for instance fleets\. The On\-Demand units are not allowed to scale beyond this boundary\. The parameter is used to split capacity allocation between On\-Demand and Spot Instances\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumCapacityUnits`  <a name="cfn-elasticmapreduce-cluster-computelimits-minimumcapacityunits"></a>
 The lower boundary of EC2 units\. It is measured through vCPU cores or instances for instance groups and measured through units for instance fleets\. Managed scaling activities are not allowed beyond this boundary\. The limit only applies to the core and task nodes\. The master node cannot be scaled after initial configuration\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnitType`  <a name="cfn-elasticmapreduce-cluster-computelimits-unittype"></a>
 The unit type used for specifying a managed scaling policy\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `InstanceFleetUnits | Instances | VCPU`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)