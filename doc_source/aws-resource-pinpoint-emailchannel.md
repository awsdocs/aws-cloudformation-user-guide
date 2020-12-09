# AWS::Pinpoint::EmailChannel<a name="aws-resource-pinpoint-emailchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the email channel to send email to users\. Before you can use Amazon Pinpoint to send email, you must enable the email channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::EmailChannel resource defines the status, identity, and other settings of the email channel for an application\.

## Syntax<a name="aws-resource-pinpoint-emailchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-emailchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::EmailChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-emailchannel-applicationid)" : String,
      "[ConfigurationSet](#cfn-pinpoint-emailchannel-configurationset)" : String,
      "[Enabled](#cfn-pinpoint-emailchannel-enabled)" : Boolean,
      "[FromAddress](#cfn-pinpoint-emailchannel-fromaddress)" : String,
      "[Identity](#cfn-pinpoint-emailchannel-identity)" : String,
      "[RoleArn](#cfn-pinpoint-emailchannel-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-emailchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::EmailChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-emailchannel-applicationid): String
  [ConfigurationSet](#cfn-pinpoint-emailchannel-configurationset): String
  [Enabled](#cfn-pinpoint-emailchannel-enabled): Boolean
  [FromAddress](#cfn-pinpoint-emailchannel-fromaddress): String
  [Identity](#cfn-pinpoint-emailchannel-identity): String
  [RoleArn](#cfn-pinpoint-emailchannel-rolearn): String
```

## Properties<a name="aws-resource-pinpoint-emailchannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-emailchannel-applicationid"></a>
The unique identifier for the application that the email channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationSet`  <a name="cfn-pinpoint-emailchannel-configurationset"></a>
The configuration set that you want to apply to email that you send through the channel by using the Amazon Pinpoint Email API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-emailchannel-enabled"></a>
Specifies whether to enable the email channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromAddress`  <a name="cfn-pinpoint-emailchannel-fromaddress"></a>
The verified email address that you want to send email from when you send email through the channel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Identity`  <a name="cfn-pinpoint-emailchannel-identity"></a>
The Amazon Resource Name \(ARN\) of the identity, verified with Amazon Simple Email Service \(Amazon SES\), that you want to use when you send email through the channel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-pinpoint-emailchannel-rolearn"></a>
The ARN of the AWS Identity and Access Management \(IAM\) role that you want Amazon Pinpoint to use when it submits email\-related event data for the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-emailchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-emailchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.