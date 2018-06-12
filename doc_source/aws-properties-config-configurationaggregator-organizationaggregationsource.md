# AWS Config ConfigurationAggregator OrganizationAggregationSource<a name="aws-properties-config-configurationaggregator-organizationaggregationsource"></a>

<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-description"></a>The `OrganizationAggregationSource` property type specifies the regions of AWS Config data to aggregate into an AWS Config configuration aggregator and the IAM role to use to retrieve AWS Organizations details\.

<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-inheritance"></a>The `OrganizationAggregationSources` property of the [AWS::Config::ConfigurationAggregator](aws-resource-config-configurationaggregator.md) resource contains a list of `OrganizationAggregationSource` property types\.

## Syntax<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-syntax.json"></a>

```
{
  "[AllAwsRegions](#cfn-config-configurationaggregator-organizationaggregationsource-allawsregions)" : Boolean,
  "[AwsRegions](#cfn-config-configurationaggregator-organizationaggregationsource-awsregions)" : [ String, ... ],
  "[RoleArn](#cfn-config-configurationaggregator-organizationaggregationsource-rolearn)" : String
}
```

### YAML<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-syntax.yaml"></a>

```
[AllAwsRegions](#cfn-config-configurationaggregator-organizationaggregationsource-allawsregions): Boolean
[AwsRegions](#cfn-config-configurationaggregator-organizationaggregationsource-awsregions): 
  - String
[RoleArn](#cfn-config-configurationaggregator-organizationaggregationsource-rolearn): 
  String
```

## Properties<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-properties"></a>

`AllAwsRegions`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-allawsregions"></a>
If `true` aggreagate existing AWS Config regions and future regions\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsRegions`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-awsregions"></a>
The source regions being aggregated\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleArn`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used to retreive AWS Organizations details associated with the aggregator account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 