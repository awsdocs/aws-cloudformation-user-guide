# Amazon EMR InstanceFleetConfig InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications"></a>

Use the `InstanceFleetProvisioningSpecifications` property type to create or modify the launch specification for Spot Instances in the fleet\. This determines the defined duration and provisioning timeout behavior\. `InstanceFleetProvisioningSpecifications` is the property type for the `LaunchSpecifications` property of the [AWS::EMR::InstanceFleetConfig](aws-resource-elasticmapreduce-instancefleetconfig.md) resource\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[SpotSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification)" : [*SpotProvisioningSpecification*](aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification.md)
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
[SpotSpecification](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification):
  [*SpotProvisioningSpecification*](aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification.md)
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-properties"></a>

`SpotSpecification`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification"></a>
The launch specification for Spot Instances in the fleet\. This determines the defined duration and provisioning timeout behavior\.  
*Required*: Yes  
*Type*: [Amazon EMR InstanceFleetConfig SpotProvisioningSpecification](aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)