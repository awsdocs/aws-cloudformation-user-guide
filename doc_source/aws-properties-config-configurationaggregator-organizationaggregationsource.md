# AWS::Config::ConfigurationAggregator OrganizationAggregationSource<a name="aws-properties-config-configurationaggregator-organizationaggregationsource"></a>

This object contains regions to set up the aggregator and an IAM role to retrieve organization details\.

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
  [RoleArn](#cfn-config-configurationaggregator-organizationaggregationsource-rolearn): String
```

## Properties<a name="aws-properties-config-configurationaggregator-organizationaggregationsource-properties"></a>

`AllAwsRegions`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-allawsregions"></a>
If true, aggregate existing AWS Config regions and future regions\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsRegions`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-awsregions"></a>
The source regions being aggregated\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-config-configurationaggregator-organizationaggregationsource-rolearn"></a>
ARN of the IAM role used to retrieve AWS Organization details associated with the aggregator account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)