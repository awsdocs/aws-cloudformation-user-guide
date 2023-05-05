# AWS::GuardDuty::Detector FeatureAdditionalConfiguration<a name="aws-properties-guardduty-detector-featureadditionalconfiguration"></a>

Describes the additional configuration for a feature\. If you want to specify any additional configuration for your feature, it is required to provide the `Name` and `Status` for that additional configuration\. For more information, see [DetectorAdditionalConfiguration](https://docs.aws.amazon.com/guardduty/latest/APIReference/API_DetectorAdditionalConfiguration.html)\.

If you're providing additional configuration, ensure to provide the corresponding [FeatureConfigurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-guardduty-detector-featureconfigurations.html#cfn-guardduty-detector-featureconfigurations-additionalconfiguration)\.

## Syntax<a name="aws-properties-guardduty-detector-featureadditionalconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-featureadditionalconfiguration-syntax.json"></a>

```
{
  "[Name](#cfn-guardduty-detector-featureadditionalconfiguration-name)" : String,
  "[Status](#cfn-guardduty-detector-featureadditionalconfiguration-status)" : String
}
```

### YAML<a name="aws-properties-guardduty-detector-featureadditionalconfiguration-syntax.yaml"></a>

```
  [Name](#cfn-guardduty-detector-featureadditionalconfiguration-name): String
  [Status](#cfn-guardduty-detector-featureadditionalconfiguration-status): String
```

## Properties<a name="aws-properties-guardduty-detector-featureadditionalconfiguration-properties"></a>

`Name`  <a name="cfn-guardduty-detector-featureadditionalconfiguration-name"></a>
Name of the additional configuration of a feature\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-guardduty-detector-featureadditionalconfiguration-status"></a>
Status of the additional configuration of a feature\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)