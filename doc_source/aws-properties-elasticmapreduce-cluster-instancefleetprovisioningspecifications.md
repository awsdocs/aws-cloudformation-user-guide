# AWS::EMR::Cluster InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications"></a>

`InstanceFleetProvisioningSpecification` is a subproperty of `InstanceFleetConfig`\. `InstanceFleetProvisioningSpecification` defines the launch specification for Spot instances in an instance fleet, which determines the defined duration and provisioning timeout behavior for Spot instances\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification)" : SpotProvisioningSpecification
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
  [SpotSpecification](#cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification): 
    SpotProvisioningSpecification
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications-properties"></a>

`SpotSpecification`  <a name="cfn-elasticmapreduce-cluster-instancefleetprovisioningspecifications-spotspecification"></a>
The launch specification for Spot instances in the fleet, which determines the defined duration, provisioning timeout behavior, and allocation strategy\.  
*Required*: Yes  
*Type*: [SpotProvisioningSpecification](aws-properties-elasticmapreduce-cluster-spotprovisioningspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)