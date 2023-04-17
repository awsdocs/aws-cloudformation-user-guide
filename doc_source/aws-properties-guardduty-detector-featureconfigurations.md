# AWS::GuardDuty::Detector FeatureConfigurations<a name="aws-properties-guardduty-detector-featureconfigurations"></a>

Describes the configuration for a feature\. Make sure you use either `dataSources` or `Features`, and not both\.

## Syntax<a name="aws-properties-guardduty-detector-featureconfigurations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-featureconfigurations-syntax.json"></a>

```
{
  "[AdditionalConfiguration](#cfn-guardduty-detector-featureconfigurations-additionalconfiguration)" : [ FeatureAdditionalConfiguration, ... ],
  "[Name](#cfn-guardduty-detector-featureconfigurations-name)" : String,
  "[Status](#cfn-guardduty-detector-featureconfigurations-status)" : String
}
```

### YAML<a name="aws-properties-guardduty-detector-featureconfigurations-syntax.yaml"></a>

```
  [AdditionalConfiguration](#cfn-guardduty-detector-featureconfigurations-additionalconfiguration): 
    - FeatureAdditionalConfiguration
  [Name](#cfn-guardduty-detector-featureconfigurations-name): String
  [Status](#cfn-guardduty-detector-featureconfigurations-status): String
```

## Properties<a name="aws-properties-guardduty-detector-featureconfigurations-properties"></a>

`AdditionalConfiguration`  <a name="cfn-guardduty-detector-featureconfigurations-additionalconfiguration"></a>
Additional configuration of the feature\.  
*Required*: No  
*Type*: List of [FeatureAdditionalConfiguration](aws-properties-guardduty-detector-featureadditionalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-guardduty-detector-featureconfigurations-name"></a>
Name of the feature\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-guardduty-detector-featureconfigurations-status"></a>
Status of the feature\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)