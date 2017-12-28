# Amazon EMR Cluster SpotProvisioningSpecification<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification"></a>

The `SpotProvisioningSpecification` property specifies the duration and timeout behavior for Spot instances in the instance fleet for Amazon EMR\. `SpotProvisioningSpecification` is the property type for the `SpotSpecification` subproperty of the [Amazon EMR Cluster InstanceFleetProvisioningSpecifications](aws-properties-elasticmapreduce-cluster-instancefleetprovisioningspecifications.md) property type\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-blockdurationminutes)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutaction)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutdurationminutes)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-blockdurationminutes): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutaction): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-spotprovisioningspecification-timeoutdurationminutes): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-spotprovisioningspecification-properties"></a>

`BlockDurationMinutes`  
The defined duration for Spot instances \(also known as Spot blocks\) in minutes\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`TimeoutAction`  
The action to take when TargetSpotCapacity has not been fulfilled when the TimeoutDurationMinutes has expired\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`TimeoutDurationMinutes`  
The spot provisioning timeout period in minutes\. For more information, see [SpotProvisioningSpecification](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SpotProvisioningSpecification.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: No interruption