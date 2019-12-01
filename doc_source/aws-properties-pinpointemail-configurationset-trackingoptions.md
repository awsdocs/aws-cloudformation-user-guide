# AWS::PinpointEmail::ConfigurationSet TrackingOptions<a name="aws-properties-pinpointemail-configurationset-trackingoptions"></a>

An object that defines the tracking options for a configuration set\. When you use Amazon Pinpoint to send an email, it contains an invisible image that's used to track when recipients open your email\. If your email contains links, those links are changed slightly in order to track when recipients click them\.

These images and links include references to a domain operated by AWS\. You can optionally configure Amazon Pinpoint to use a domain that you operate for these images and links\.

## Syntax<a name="aws-properties-pinpointemail-configurationset-trackingoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationset-trackingoptions-syntax.json"></a>

```
{
  "[CustomRedirectDomain](#cfn-pinpointemail-configurationset-trackingoptions-customredirectdomain)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-configurationset-trackingoptions-syntax.yaml"></a>

```
  [CustomRedirectDomain](#cfn-pinpointemail-configurationset-trackingoptions-customredirectdomain): String
```

## Properties<a name="aws-properties-pinpointemail-configurationset-trackingoptions-properties"></a>

`CustomRedirectDomain`  <a name="cfn-pinpointemail-configurationset-trackingoptions-customredirectdomain"></a>
The domain that you want to use for tracking open and click events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)