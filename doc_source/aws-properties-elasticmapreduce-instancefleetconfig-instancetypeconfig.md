# Amazon EMR InstanceFleetConfig InstanceTypeConfig<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig"></a>

Use the `InstanceTypeConfig` property to configure each instance type  in an instance fleet\. This configuration determines which EC2 instances that Amazon EMR attempts to provision to fulfill On\-Demand and Spot target capacities\. You can configure a maximum of five instance types in a fleet\. For a list of `InstanceTypeConfig` property types, see the `InstanceTypeConfigs` property of the [AWS::EMR::InstanceFleetConfig](aws-resource-elasticmapreduce-instancefleetconfig.md) resource\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidprice)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidpriceaspercentageofondemandprice)" : Double,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-configurations)" : [ Configuration, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-ebsconfiguration)" : EbsConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-instancetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-weightedcapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidprice): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidpriceaspercentageofondemandprice): Double
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-configurations):
  - Configuration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-ebsconfiguration):
  EbsConfiguration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-instancetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-weightedcapacity): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-properties"></a>

For more information about each property, including constraints and valid values, see see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.

`BidPrice`  
The bid price for each EC2 Spot Instance type as defined by `InstanceType`\. `BidPrice` is expressed in USD\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`BidPriceAsPercentageOfOnDemandPrice`  
The bid price, as a percentage of the On\-Demand price, for each EC2 Spot Instance as defined by `InstanceType`\. `BidPriceAsPercentageOfOnDemandPrice` is expressed as a number\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: Double  
*Update requires*: Replacement

`Configurations`  
A configuration classification that applies when provisioning cluster instances\. You can use this property to configure applications and software that run on the cluster\. Duplicates are not allowed\.  
*Required: *No  
*Type*: List of [Amazon EMR InstanceFleetConfig Configuration](aws-properties-elasticmapreduce-instancefleetconfig-configuration.md)  
*Update requires*: Replacement

`EbsConfiguration`  
The configuration of Amazon Elastic Block Store \(Amazon EBS\) that is attached to each instance as defined by `InstanceType`\.  
*Required: *No  
*Type*: [Amazon EMR InstanceFleetConfig EbsConfiguration](aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration.md)  
*Update requires*: Replacement

`InstanceType`  
An EC2 instance type, such as `m3.xlarge`\. For constraints, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`WeightedCapacity`  
The number of units that a provisioned instance of this type provides toward fulfilling the target capacities defined in `InstanceFleetConfig`\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Replacement