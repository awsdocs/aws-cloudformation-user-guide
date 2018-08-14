# AWS::EMR::InstanceFleetConfig<a name="aws-resource-elasticmapreduce-instancefleetconfig"></a>

Use the `AWS::EMR::InstanceFleetConfig` resource to configure a Spot Instance fleet for an Amazon EMR cluster\. For more information, see [Configure Instance Fleets](http://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html) in the *Amazon EMR Management Guide*\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

**Topics**
+ [Syntax](#aws-resource-elasticmapreduce-instancefleetconfig-syntax)
+ [Properties](#w3ab2c21c10d665c11)

## Syntax<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::InstanceFleetConfig",
  "Properties" : {
    "[ClusterId](#cfn-elasticmapreduce-instancefleetconfig-clusterid)" : String,
    "[InstanceFleetType](#cfn-elasticmapreduce-instancefleetconfig-instancefleettype)" : String,
    "[InstanceTypeConfigs](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs)" : [ [*InstanceTypeConfig*](aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig.md), ... ],
    "[LaunchSpecifications](#cfn-elasticmapreduce-instancefleetconfig-launchspecifications)" : [*InstanceFleetProvisioningSpecifications*](aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications.md),
    "[Name](#cfn-elasticmapreduce-instancefleetconfig-name)" : String,
    "[TargetOnDemandCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity)" : Integer,      
    "[TargetSpotCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity)" : Integer
  }
}
```

### YAML<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax.yaml"></a>

```
Type: "AWS::EMR::InstanceFleetConfig"
Properties: 
  [ClusterId](#cfn-elasticmapreduce-instancefleetconfig-clusterid): String
  [InstanceFleetType](#cfn-elasticmapreduce-instancefleetconfig-instancefleettype): String
  [InstanceTypeConfigs](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs):
    - [*InstanceTypeConfig*](aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig.md)
  [LaunchSpecifications](#cfn-elasticmapreduce-instancefleetconfig-launchspecifications):
    [*InstanceFleetProvisioningSpecifications*](aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications.md)
  [Name](#cfn-elasticmapreduce-instancefleetconfig-name): String
  [TargetOnDemandCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity): Integer
  [TargetSpotCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity): Integer
```

## Properties<a name="w3ab2c21c10d665c11"></a>

For more information about each property, including constraints and valid values, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.

`ClusterId`  <a name="cfn-elasticmapreduce-instancefleetconfig-clusterid"></a>
The ID of the target cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceFleetType`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancefleettype"></a>
The node type that the instance fleet hosts\. Valid values are `MASTER`, `CORE`, and `TASK`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceTypeConfigs`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs"></a>
The instance type configurations that define the EC2 instances in the instance fleet\. Duplicates not allowed\.  
*Required*: No  
*Type*: List of [Amazon EMR InstanceFleetConfig InstanceTypeConfig](aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LaunchSpecifications`  <a name="cfn-elasticmapreduce-instancefleetconfig-launchspecifications"></a>
The launch specification for the instance fleet\.  
*Required*: No  
*Type*: [Amazon EMR InstanceFleetConfig InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-instancefleetconfig-name"></a>
The friendly name of the instance fleet\. For constraints, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TargetOnDemandCapacity`  <a name="cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity"></a>
The target capacity of On\-Demand units for the instance fleet\. This  determines how many On\-Demand Instances to provision\. For more information, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetSpotCapacity`  <a name="cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity"></a>
The target capacity of Spot units for the instance fleet\. This determines how many Spot Instances to provision\. For more information, see [InstanceFleetConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceFleetConfig.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)