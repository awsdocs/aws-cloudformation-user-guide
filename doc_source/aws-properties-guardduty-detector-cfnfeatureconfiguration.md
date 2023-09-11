# AWS::GuardDuty::Detector CFNFeatureConfiguration<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration"></a>

<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration-description"></a>The `CFNFeatureConfiguration` property type specifies Property description not available\. for an [AWS::GuardDuty::Detector](aws-resource-guardduty-detector.md)\.

## Syntax<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration-syntax.json"></a>

```
{
  "[AdditionalConfiguration](#cfn-guardduty-detector-cfnfeatureconfiguration-additionalconfiguration)" : [ CFNFeatureAdditionalConfiguration, ... ],
  "[Name](#cfn-guardduty-detector-cfnfeatureconfiguration-name)" : String,
  "[Status](#cfn-guardduty-detector-cfnfeatureconfiguration-status)" : String
}
```

### YAML<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration-syntax.yaml"></a>

```
  [AdditionalConfiguration](#cfn-guardduty-detector-cfnfeatureconfiguration-additionalconfiguration): 
    - CFNFeatureAdditionalConfiguration
  [Name](#cfn-guardduty-detector-cfnfeatureconfiguration-name): String
  [Status](#cfn-guardduty-detector-cfnfeatureconfiguration-status): String
```

## Properties<a name="aws-properties-guardduty-detector-cfnfeatureconfiguration-properties"></a>

`AdditionalConfiguration`  <a name="cfn-guardduty-detector-cfnfeatureconfiguration-additionalconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [CFNFeatureAdditionalConfiguration](aws-properties-guardduty-detector-cfnfeatureadditionalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-guardduty-detector-cfnfeatureconfiguration-name"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-guardduty-detector-cfnfeatureconfiguration-status"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)