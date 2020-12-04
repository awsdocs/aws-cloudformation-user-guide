# AWS::EMR::InstanceFleetConfig<a name="aws-resource-elasticmapreduce-instancefleetconfig"></a>

Use `InstanceFleetConfig` to define instance fleets for an EMR cluster\. A cluster can not use both instance fleets and instance groups\. For more information, see [Configure Instance Fleets](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-group-configuration.html) in the *Amazon EMR Management Guide*\. 

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::InstanceFleetConfig",
  "Properties" : {
      "[ClusterId](#cfn-elasticmapreduce-instancefleetconfig-clusterid)" : String,
      "[InstanceFleetType](#cfn-elasticmapreduce-instancefleetconfig-instancefleettype)" : String,
      "[InstanceTypeConfigs](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs)" : [ InstanceTypeConfig, ... ],
      "[LaunchSpecifications](#cfn-elasticmapreduce-instancefleetconfig-launchspecifications)" : InstanceFleetProvisioningSpecifications,
      "[Name](#cfn-elasticmapreduce-instancefleetconfig-name)" : String,
      "[TargetOnDemandCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity)" : Integer,
      "[TargetSpotCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity)" : Integer
    }
}
```

### YAML<a name="aws-resource-elasticmapreduce-instancefleetconfig-syntax.yaml"></a>

```
Type: AWS::EMR::InstanceFleetConfig
Properties: 
  [ClusterId](#cfn-elasticmapreduce-instancefleetconfig-clusterid): String
  [InstanceFleetType](#cfn-elasticmapreduce-instancefleetconfig-instancefleettype): String
  [InstanceTypeConfigs](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs): 
    - InstanceTypeConfig
  [LaunchSpecifications](#cfn-elasticmapreduce-instancefleetconfig-launchspecifications): 
    InstanceFleetProvisioningSpecifications
  [Name](#cfn-elasticmapreduce-instancefleetconfig-name): String
  [TargetOnDemandCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity): Integer
  [TargetSpotCapacity](#cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity): Integer
```

## Properties<a name="aws-resource-elasticmapreduce-instancefleetconfig-properties"></a>

`ClusterId`  <a name="cfn-elasticmapreduce-instancefleetconfig-clusterid"></a>
The unique identifier of the EMR cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceFleetType`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancefleettype"></a>
The node type that the instance fleet hosts\. Valid values are MASTER,CORE,and TASK\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CORE | MASTER | TASK`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceTypeConfigs`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfigs"></a>
`InstanceTypeConfigs` determine the EC2 instances that Amazon EMR attempts to provision to fulfill On\-Demand and Spot target capacities\. There can be a maximum of 5 instance type configurations in a fleet, each one specified using an `InstanceTypeConfig`\.  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.
*Required*: No  
*Type*: List of [InstanceTypeConfig](aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchSpecifications`  <a name="cfn-elasticmapreduce-instancefleetconfig-launchspecifications"></a>
The launch specification for the instance fleet\.  
*Required*: No  
*Type*: [InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-instancefleetconfig-name"></a>
The friendly name of the instance fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetOnDemandCapacity`  <a name="cfn-elasticmapreduce-instancefleetconfig-targetondemandcapacity"></a>
The target capacity of On\-Demand units for the instance fleet, which determines how many On\-Demand instances to provision\. When the instance fleet launches, Amazon EMR tries to provision On\-Demand instances as specified by `InstanceTypeConfig`\. Each instance configuration has a specified `WeightedCapacity`\. When an On\-Demand instance is provisioned, the `WeightedCapacity` units count toward the target capacity\. Amazon EMR provisions instances until the target capacity is totally fulfilled, even if this results in an overage\. For example, if there are 2 units remaining to fulfill capacity, and Amazon EMR can only provision an instance with a `WeightedCapacity` of 5 units, the instance is provisioned, and the target capacity is exceeded by 3 units\.  
If not specified or set to 0, only Spot instances are provisioned for the instance fleet using `TargetSpotCapacity`\. At least one of `TargetSpotCapacity` and `TargetOnDemandCapacity` should be greater than 0\. For a master instance fleet, only one of `TargetSpotCapacity` and `TargetOnDemandCapacity` can be specified, and its value must be 1\.
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetSpotCapacity`  <a name="cfn-elasticmapreduce-instancefleetconfig-targetspotcapacity"></a>
The target capacity of Spot units for the instance fleet, which determines how many Spot instances to provision\. When the instance fleet launches, Amazon EMR tries to provision Spot instances as specified by `InstanceTypeConfig`\. Each instance configuration has a specified `WeightedCapacity`\. When a Spot instance is provisioned, the `WeightedCapacity` units count toward the target capacity\. Amazon EMR provisions instances until the target capacity is totally fulfilled, even if this results in an overage\. For example, if there are 2 units remaining to fulfill capacity, and Amazon EMR can only provision an instance with a `WeightedCapacity` of 5 units, the instance is provisioned, and the target capacity is exceeded by 3 units\.  
If not specified or set to 0, only On\-Demand instances are provisioned for the instance fleet\. At least one of `TargetSpotCapacity` and `TargetOnDemandCapacity` should be greater than 0\. For a master instance fleet, only one of `TargetSpotCapacity` and `TargetOnDemandCapacity` can be specified, and its value must be 1\.
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticmapreduce-instancefleetconfig-return-values"></a>

### Ref<a name="aws-resource-elasticmapreduce-instancefleetconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns returns the ID of the instance fleet\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.