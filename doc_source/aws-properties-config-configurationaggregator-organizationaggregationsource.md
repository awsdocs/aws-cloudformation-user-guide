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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
