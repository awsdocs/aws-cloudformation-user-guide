# Amazon EMR InstanceFleetConfig InstanceFleetProvisioningSpecifications<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications"></a>

Use the `InstanceFleetProvisioningSpecifications` property type to create or modify the launch specification for Spot Instances in the fleet\. This determines the defined duration and provisioning timeout behavior\. `InstanceFleetProvisioningSpecifications` is the property type for the `LaunchSpecifications` property of the [AWS::EMR::InstanceFleetConfig](aws-resource-elasticmapreduce-instancefleetconfig.md) resource\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification)" : SpotProvisioningSpecification
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-spotspecification):
  SpotProvisioningSpecification
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications-properties"></a>

`SpotSpecification`  
The launch specification for Spot Instances in the fleet\. This determines the defined duration and provisioning timeout behavior\.  
*Required: *Yes  
*Type*: [Amazon EMR InstanceFleetConfig SpotProvisioningSpecification](aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification.md)  
*Update requires*: No interruption