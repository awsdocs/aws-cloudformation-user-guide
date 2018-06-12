# AWS Config ConfigurationAggregator AccountAggregationSource<a name="aws-properties-config-configurationaggregator-accountaggregationsource"></a>

<a name="aws-properties-config-configurationaggregator-accountaggregationsource-description"></a>The `AccountAggregationSource` property type specifies the accounts and regions of AWS Config data to aggregate into an AWS Config configuration aggregator\.

<a name="aws-properties-config-configurationaggregator-accountaggregationsource-inheritance"></a>The `AccountAggregationSources` property of the [AWS::Config::ConfigurationAggregator](aws-resource-config-configurationaggregator.md) resource contains a list of `AccountAggregationSource` property types\.

## Syntax<a name="aws-properties-config-configurationaggregator-accountaggregationsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationaggregator-accountaggregationsource-syntax.json"></a>

```
{
  "[AllAwsRegions](#cfn-config-configurationaggregator-accountaggregationsource-allawsregions)" : Boolean,
  "[AwsRegions](#cfn-config-configurationaggregator-accountaggregationsource-awsregions)" : [ String, ... ],
  "[AccountIds](#cfn-config-configurationaggregator-accountaggregationsource-accountids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-configurationaggregator-accountaggregationsource-syntax.yaml"></a>

```
[AllAwsRegions](#cfn-config-configurationaggregator-accountaggregationsource-allawsregions): Boolean
[AwsRegions](#cfn-config-configurationaggregator-accountaggregationsource-awsregions): 
  - String
[AccountIds](#cfn-config-configurationaggregator-accountaggregationsource-accountids): 
  - String
```

## Properties<a name="aws-properties-config-configurationaggregator-accountaggregationsource-properties"></a>

`AllAwsRegions`  <a name="cfn-config-configurationaggregator-accountaggregationsource-allawsregions"></a>
If true aggreagate existing AWS Config regions and future regions\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsRegions`  <a name="cfn-config-configurationaggregator-accountaggregationsource-awsregions"></a>
The source regions being aggregated\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AccountIds`  <a name="cfn-config-configurationaggregator-accountaggregationsource-accountids"></a>
The 12 digit account ID of the account being aggregated\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 