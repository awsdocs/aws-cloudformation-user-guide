# AWS::SES::ConfigurationSet<a name="aws-resource-ses-configurationset"></a>

Configuration sets let you create groups of rules that you can apply to the emails you send using Amazon SES\. For more information about using configuration sets, see [Using Amazon SES Configuration Sets](https://docs.aws.amazon.com/ses/latest/dg/using-configuration-sets.html) in the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/dg/)\.

**Note**  
**Required permissions:**  
To apply any of the resource options, you will need to have the corresponding AWS Identity and Access Management \(IAM\) SES API v2 permissions:  
`ses:GetConfigurationSet`  
\(This permission is replacing the v1 *ses:DescribeConfigurationSet* permission which will not work with these v2 resource options\.\)
`ses:PutConfigurationSetDeliveryOptions`
`ses:PutConfigurationSetReputationOptions`
`ses:PutConfigurationSetSendingOptions`
`ses:PutConfigurationSetSuppressionOptions`
`ses:PutConfigurationSetTrackingOptions`

## Syntax<a name="aws-resource-ses-configurationset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-configurationset-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ConfigurationSet",
  "Properties" : {
      "[DeliveryOptions](#cfn-ses-configurationset-deliveryoptions)" : DeliveryOptions,
      "[Name](#cfn-ses-configurationset-name)" : String,
      "[ReputationOptions](#cfn-ses-configurationset-reputationoptions)" : ReputationOptions,
      "[SendingOptions](#cfn-ses-configurationset-sendingoptions)" : SendingOptions,
      "[SuppressionOptions](#cfn-ses-configurationset-suppressionoptions)" : SuppressionOptions,
      "[TrackingOptions](#cfn-ses-configurationset-trackingoptions)" : TrackingOptions,
      "[VdmOptions](#cfn-ses-configurationset-vdmoptions)" : VdmOptions
    }
}
```

### YAML<a name="aws-resource-ses-configurationset-syntax.yaml"></a>

```
Type: AWS::SES::ConfigurationSet
Properties: 
  [DeliveryOptions](#cfn-ses-configurationset-deliveryoptions): 
    DeliveryOptions
  [Name](#cfn-ses-configurationset-name): String
  [ReputationOptions](#cfn-ses-configurationset-reputationoptions): 
    ReputationOptions
  [SendingOptions](#cfn-ses-configurationset-sendingoptions): 
    SendingOptions
  [SuppressionOptions](#cfn-ses-configurationset-suppressionoptions): 
    SuppressionOptions
  [TrackingOptions](#cfn-ses-configurationset-trackingoptions): 
    TrackingOptions
  [VdmOptions](#cfn-ses-configurationset-vdmoptions): 
    VdmOptions
```

## Properties<a name="aws-resource-ses-configurationset-properties"></a>

`DeliveryOptions`  <a name="cfn-ses-configurationset-deliveryoptions"></a>
Specifies whether messages that use the configuration set are required to use Transport Layer Security \(TLS\)\.  
*Required*: No  
*Type*: [DeliveryOptions](aws-properties-ses-configurationset-deliveryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ses-configurationset-name"></a>
The name of the configuration set\. The name must meet the following requirements:  
+ Contain only letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 64 characters or fewer\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReputationOptions`  <a name="cfn-ses-configurationset-reputationoptions"></a>
An object that represents the reputation settings for the configuration set\.   
*Required*: No  
*Type*: [ReputationOptions](aws-properties-ses-configurationset-reputationoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SendingOptions`  <a name="cfn-ses-configurationset-sendingoptions"></a>
An object that defines whether or not Amazon SES can send email that you send using the configuration set\.  
*Required*: No  
*Type*: [SendingOptions](aws-properties-ses-configurationset-sendingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuppressionOptions`  <a name="cfn-ses-configurationset-suppressionoptions"></a>
An object that contains information about the suppression list preferences for your account\.  
*Required*: No  
*Type*: [SuppressionOptions](aws-properties-ses-configurationset-suppressionoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrackingOptions`  <a name="cfn-ses-configurationset-trackingoptions"></a>
The name of the custom open and click tracking domain associated with the configuration set\.  
*Required*: No  
*Type*: [TrackingOptions](aws-properties-ses-configurationset-trackingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VdmOptions`  <a name="cfn-ses-configurationset-vdmoptions"></a>
The Virtual Deliverability Manager \(VDM\) options that apply to the configuration set\.  
*Required*: No  
*Type*: [VdmOptions](aws-properties-ses-configurationset-vdmoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ses-configurationset-return-values"></a>

### Ref<a name="aws-resource-ses-configurationset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ses-configurationset--examples"></a>



### <a name="aws-resource-ses-configurationset--examples--"></a>

Specifies a configuration set\.

#### JSON<a name="aws-resource-ses-configurationset--examples----json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ConfigurationSet Sample Template",
    "Parameters": {
        "ConfigSetName": {
            "Type": "String"
        }
    },
    "Resources": {
        "ConfigSet": {
            "Type": "AWS::SES::ConfigurationSet",
            "Properties": {
                "Name": {
                    "Ref": "ConfigSetName"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-configurationset--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES ConfigurationSet Sample Template
Parameters:
  ConfigSetName:
    Type: String
Resources:
  ConfigSet:
    Type: 'AWS::SES::ConfigurationSet'
    Properties:
      Name: !Ref ConfigSetName
```