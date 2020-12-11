# AWS::EMR::InstanceFleetConfig InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications"></a>

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

`InstanceTypeConfig` is a sub\-property of `InstanceFleetConfig`\. `InstanceTypeConfig` determines the EC2 instances that Amazon EMR attempts to provision to fulfill On\-Demand and Spot target capacities\. There can be a maximum of 5 instance type configurations in a fleet\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[OnDemandSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-ondemandspecification)" : OnDemandProvisioningSpecification,
  "[SpotSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification)" : SpotProvisioningSpecification
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
  [OnDemandSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-ondemandspecification): 
    OnDemandProvisioningSpecification
  [SpotSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification): 
    SpotProvisioningSpecification
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-properties"></a>

`OnDemandSpecification`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-ondemandspecification"></a>
 The launch specification for On\-Demand Instances in the instance fleet, which determines the allocation strategy\.   
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\. On\-Demand Instances allocation strategy is available in Amazon EMR version 5\.12\.1 and later\.
*Required*: No  
*Type*: [OnDemandProvisioningSpecification](aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotSpecification`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification"></a>
The launch specification for Spot Instances in the fleet, which determines the defined duration, provisioning timeout behavior, and allocation strategy\.  
*Required*: No  
*Type*: [SpotProvisioningSpecification](aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)