# AWS::EMR::Cluster InstanceFleetConfig<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig"></a>

Use `InstanceFleetConfig` to define instance fleets for an EMR cluster\. A cluster can not use both instance fleets and instance groups\. For more information, see [Configure Instance Fleets](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-group-configuration.html) in the *Amazon EMR Management Guide*\. 

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-syntax.json"></a>

```
{
  "[InstanceTypeConfigs](#cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs)" : [ InstanceTypeConfig, ... ],
  "[LaunchSpecifications](#cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications)" : InstanceFleetProvisioningSpecifications,
  "[Name](#cfn-elasticmapreduce-cluster-instancefleetconfig-name)" : String,
  "[TargetOnDemandCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity)" : Integer,
  "[TargetSpotCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-syntax.yaml"></a>

```
  [InstanceTypeConfigs](#cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs): 
    - InstanceTypeConfig
  [LaunchSpecifications](#cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications): 
    InstanceFleetProvisioningSpecifications
  [Name](#cfn-elasticmapreduce-cluster-instancefleetconfig-name): String
  [TargetOnDemandCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity): Integer
  [TargetSpotCapacity](#cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancefleetconfig-properties"></a>

`InstanceTypeConfigs`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-instancetypeconfigs"></a>
The instance type configurations that define the EC2 instances in the instance fleet\.  
*Required*: No  
*Type*: List of [InstanceTypeConfig](aws-properties-elasticmapreduce-cluster-instancetypeconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchSpecifications`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-launchspecifications"></a>
The launch specification for the instance fleet\.  
*Required*: No  
*Type*: [InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-name"></a>
The friendly name of the instance fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetOnDemandCapacity`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-targetondemandcapacity"></a>
The target capacity of On\-Demand units for the instance fleet, which determines how many On\-Demand instances to provision\. When the instance fleet launches, Amazon EMR tries to provision On\-Demand instances as specified by `InstanceTypeConfig`\. Each instance configuration has a specified `WeightedCapacity`\. When an On\-Demand instance is provisioned, the `WeightedCapacity` units count toward the target capacity\. Amazon EMR provisions instances until the target capacity is totally fulfilled, even if this results in an overage\. For example, if there are 2 units remaining to fulfill capacity, and Amazon EMR can only provision an instance with a `WeightedCapacity` of 5 units, the instance is provisioned, and the target capacity is exceeded by 3 units\.  
If not specified or set to 0, only Spot instances are provisioned for the instance fleet using `TargetSpotCapacity`\. At least one of `TargetSpotCapacity` and `TargetOnDemandCapacity` should be greater than 0\. For a master instance fleet, only one of `TargetSpotCapacity` and `TargetOnDemandCapacity` can be specified, and its value must be 1\.
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetSpotCapacity`  <a name="cfn-elasticmapreduce-cluster-instancefleetconfig-targetspotcapacity"></a>
The target capacity of Spot units for the instance fleet, which determines how many Spot instances to provision\. When the instance fleet launches, Amazon EMR tries to provision Spot instances as specified by `InstanceTypeConfig`\. Each instance configuration has a specified `WeightedCapacity`\. When a Spot instance is provisioned, the `WeightedCapacity` units count toward the target capacity\. Amazon EMR provisions instances until the target capacity is totally fulfilled, even if this results in an overage\. For example, if there are 2 units remaining to fulfill capacity, and Amazon EMR can only provision an instance with a `WeightedCapacity` of 5 units, the instance is provisioned, and the target capacity is exceeded by 3 units\.  
If not specified or set to 0, only On\-Demand instances are provisioned for the instance fleet\. At least one of `TargetSpotCapacity` and `TargetOnDemandCapacity` should be greater than 0\. For a master instance fleet, only one of `TargetSpotCapacity` and `TargetOnDemandCapacity` can be specified, and its value must be 1\.
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)