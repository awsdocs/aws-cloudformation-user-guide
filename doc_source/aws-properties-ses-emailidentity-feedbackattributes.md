# AWS::SES::EmailIdentity FeedbackAttributes<a name="aws-properties-ses-emailidentity-feedbackattributes"></a>

Used to enable or disable feedback forwarding for an identity\. This setting determines what happens when an identity is used to send an email that results in a bounce or complaint event\.

## Syntax<a name="aws-properties-ses-emailidentity-feedbackattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-emailidentity-feedbackattributes-syntax.json"></a>

```
{
  "[EmailForwardingEnabled](#cfn-ses-emailidentity-feedbackattributes-emailforwardingenabled)" : Boolean
}
```

### YAML<a name="aws-properties-ses-emailidentity-feedbackattributes-syntax.yaml"></a>

```
  [EmailForwardingEnabled](#cfn-ses-emailidentity-feedbackattributes-emailforwardingenabled): Boolean
```

## Properties<a name="aws-properties-ses-emailidentity-feedbackattributes-properties"></a>

`EmailForwardingEnabled`  <a name="cfn-ses-emailidentity-feedbackattributes-emailforwardingenabled"></a>
Sets the feedback forwarding configuration for the identity\.  
 If the value is `true`, you receive email notifications when bounce or complaint events occur\. These notifications are sent to the address that you specified in the `Return-Path` header of the original email\.  
 You're required to have a method of tracking bounces and complaints\. If you haven't set up another mechanism for receiving bounce or complaint notifications \(for example, by setting up an event destination\), you receive an email notification when these events occur \(even if this setting is disabled\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)