# AWS::EMR::InstanceFleetConfig InstanceTypeConfig<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig"></a>

`InstanceType` config is a subproperty of `InstanceFleetConfig`\. An instance type configuration specifies each instance type in an instance fleet\. The configuration determines the EC2 instances Amazon EMR attempts to provision to fulfill On\-Demand and Spot target capacities\. There can be a maximum of 5 instance type configurations in a fleet\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax.json"></a>

```
{
  "[BidPrice](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidprice)" : String,
  "[BidPriceAsPercentageOfOnDemandPrice](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidpriceaspercentageofondemandprice)" : Double,
  "[Configurations](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-configurations)" : [ Configuration, ... ],
  "[EbsConfiguration](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-ebsconfiguration)" : EbsConfiguration,
  "[InstanceType](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-instancetype)" : String,
  "[WeightedCapacity](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-weightedcapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-syntax.yaml"></a>

```
  [BidPrice](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidprice): String
  [BidPriceAsPercentageOfOnDemandPrice](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidpriceaspercentageofondemandprice): Double
  [Configurations](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-configurations): 
    - Configuration
  [EbsConfiguration](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-ebsconfiguration): 
    EbsConfiguration
  [InstanceType](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-instancetype): String
  [WeightedCapacity](#cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-weightedcapacity): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig-properties"></a>

`BidPrice`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidprice"></a>
The bid price for each EC2 Spot Instance type as defined by `InstanceType`\. Expressed in USD\. If neither `BidPrice` nor `BidPriceAsPercentageOfOnDemandPrice` is provided, `BidPriceAsPercentageOfOnDemandPrice` defaults to 100%\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BidPriceAsPercentageOfOnDemandPrice`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-bidpriceaspercentageofondemandprice"></a>
The bid price, as a percentage of On\-Demand price, for each EC2 Spot Instance as defined by `InstanceType`\. Expressed as a number \(for example, 20 specifies 20%\)\. If neither `BidPrice` nor `BidPriceAsPercentageOfOnDemandPrice` is provided, `BidPriceAsPercentageOfOnDemandPrice` defaults to 100%\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configurations`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-configurations"></a>
Amazon EMR releases 4\.x or later\.
An optional configuration specification to be used when provisioning cluster instances, which can include configurations for applications and software bundled with Amazon EMR\. A configuration consists of a classification, properties, and optional nested configurations\. A classification refers to an application\-specific configuration file\. Properties are the settings you want to change in that file\. For more information, see [Configuring Applications](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html)\.  
*Required*: No  
*Type*: List of [Configuration](aws-properties-elasticmapreduce-instancefleetconfig-configuration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsConfiguration`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-ebsconfiguration"></a>
The configuration of Amazon Elastic Block Storage \(Amazon EBS\) attached to each instance as defined by `InstanceType`\.   
*Required*: No  
*Type*: [EbsConfiguration](aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-instancetype"></a>
An EC2 instance type, such as `m3.xlarge`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeightedCapacity`  <a name="cfn-elasticmapreduce-instancefleetconfig-instancetypeconfig-weightedcapacity"></a>
The number of units that a provisioned instance of this type provides toward fulfilling the target capacities defined in `InstanceFleetConfig`\. This value is 1 for a master instance fleet, and must be 1 or greater for core and task instance fleets\. Defaults to 1 if not specified\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)