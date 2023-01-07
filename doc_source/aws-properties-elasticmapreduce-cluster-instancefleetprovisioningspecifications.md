# AWS::EMR::Cluster InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications"></a>

`InstanceFleetProvisioningSpecification` is a subproperty of `InstanceFleetConfig`\. `InstanceFleetProvisioningSpecification` defines the launch specification for Spot instances in an instance fleet, which determines the defined duration and provisioning timeout behavior for Spot instances\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[OnDemandSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-ondemandspecification)" : OnDemandProvisioningSpecification,
  "[SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification)" : SpotProvisioningSpecification
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
  [OnDemandSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-ondemandspecification): 
    OnDemandProvisioningSpecification
  [SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification): 
    SpotProvisioningSpecification
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-properties"></a>

`OnDemandSpecification`  <a name="cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-ondemandspecification"></a>
 The launch specification for On\-Demand Instances in the instance fleet, which determines the allocation strategy\.   
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\. On\-Demand Instances allocation strategy is available in Amazon EMR version 5\.12\.1 and later\.
*Required*: No  
*Type*: [OnDemandProvisioningSpecification](aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotSpecification`  <a name="cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification"></a>
The launch specification for Spot Instances in the fleet, which determines the defined duration, provisioning timeout behavior, and allocation strategy\.  
*Required*: No  
*Type*: [SpotProvisioningSpecification](aws-properties-elasticmapreduce-cluster-spotprovisioningspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)