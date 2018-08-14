# Amazon EMR Cluster InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications"></a>

The `InstanceFleetProvisioningSpecifications` property specifies the launch specification for Spot instances in the fleet, which determines the defined duration and provisioning timeout behavior\. `InstanceFleetProvisioningSpecifications` is the property type for the `LaunchSpecifications` property of the [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md) property type\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification)" : [*SpotProvisioningSpecification*](aws-properties-elasticmapreduce-cluster-spotprovisioningspecification.md)
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
[SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification): 
  [*SpotProvisioningSpecification*](aws-properties-elasticmapreduce-cluster-spotprovisioningspecification.md)
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-properties"></a>

`SpotSpecification`  <a name="cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification"></a>
The launch specification for Spot instances in the fleet, which determines the defined duration and provisioning timeout behavior\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster SpotProvisioningSpecification](aws-properties-elasticmapreduce-cluster-spotprovisioningspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)