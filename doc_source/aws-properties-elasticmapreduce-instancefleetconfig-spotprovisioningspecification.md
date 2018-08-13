# Amazon EMR InstanceFleetConfig SpotProvisioningSpecification<a name="aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification"></a>

Use the `SpotProvisioningSpecification` property to specify the duration and timeout behavior for Spot Instances in the instance fleet for Amazon EMR\. `SpotProvisioningSpecification` is the property type for the `SpotSpecification` subproperty of the [Amazon EMR InstanceFleetConfig InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-instancefleetconfig-instancefleetprovisioningspecifications.md) property type\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-syntax.json"></a>

```
{
  "[BlockDurationMinutes](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-blockdurationminutes)" : Integer,
  "[TimeoutAction](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutaction)" : String,
  "[TimeoutDurationMinutes](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutdurationminutes)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-syntax.yaml"></a>

```
[BlockDurationMinutes](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-blockdurationminutes): Integer
[TimeoutAction](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutaction): String
[TimeoutDurationMinutes](#cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutdurationminutes): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-properties"></a>

`BlockDurationMinutes`  <a name="cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-blockdurationminutes"></a>
The defined duration for Spot Instances \(also known as Spot blocks\) in minutes\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimeoutAction`  <a name="cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutaction"></a>
The action to take when the capacity for the target Spot Instance, as specified in `TargetSpotCapacity`, has not been fulfilled before the time specified in `TimeoutDurationMinutes` has expired\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimeoutDurationMinutes`  <a name="cfn-elasticmapreduce-instancefleetconfig-spotprovisioningspecification-timeoutdurationminutes"></a>
The timeout period for spot provisioning, in minutes\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)