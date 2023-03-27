# AWS::SES::ConfigurationSet ReputationOptions<a name="aws-properties-ses-configurationset-reputationoptions"></a>

Contains information about the reputation settings for a configuration set\.

## Syntax<a name="aws-properties-ses-configurationset-reputationoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationset-reputationoptions-syntax.json"></a>

```
{
  "[ReputationMetricsEnabled](#cfn-ses-configurationset-reputationoptions-reputationmetricsenabled)" : Boolean
}
```

### YAML<a name="aws-properties-ses-configurationset-reputationoptions-syntax.yaml"></a>

```
  [ReputationMetricsEnabled](#cfn-ses-configurationset-reputationoptions-reputationmetricsenabled): Boolean
```

## Properties<a name="aws-properties-ses-configurationset-reputationoptions-properties"></a>

`ReputationMetricsEnabled`  <a name="cfn-ses-configurationset-reputationoptions-reputationmetricsenabled"></a>
Describes whether or not Amazon SES publishes reputation metrics for the configuration set, such as bounce and complaint rates, to Amazon CloudWatch\.  
If the value is `true`, reputation metrics are published\. If the value is `false`, reputation metrics are not published\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)