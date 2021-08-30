# AWS::SSMContacts::ContactChannel<a name="aws-resource-ssmcontacts-contactchannel"></a>

The `AWS::SSMContacts::ContactChannel` resource specifies a contact channel as the method that Incident Manager uses to engage your contact\.

## Syntax<a name="aws-resource-ssmcontacts-contactchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmcontacts-contactchannel-syntax.json"></a>

```
{
  "Type" : "AWS::SSMContacts::ContactChannel",
  "Properties" : {
      "[ChannelAddress](#cfn-ssmcontacts-contactchannel-channeladdress)" : String,
      "[ChannelName](#cfn-ssmcontacts-contactchannel-channelname)" : String,
      "[ChannelType](#cfn-ssmcontacts-contactchannel-channeltype)" : String,
      "[ContactId](#cfn-ssmcontacts-contactchannel-contactid)" : String,
      "[DeferActivation](#cfn-ssmcontacts-contactchannel-deferactivation)" : Boolean
    }
}
```

### YAML<a name="aws-resource-ssmcontacts-contactchannel-syntax.yaml"></a>

```
Type: AWS::SSMContacts::ContactChannel
Properties: 
  [ChannelAddress](#cfn-ssmcontacts-contactchannel-channeladdress): String
  [ChannelName](#cfn-ssmcontacts-contactchannel-channelname): String
  [ChannelType](#cfn-ssmcontacts-contactchannel-channeltype): String
  [ContactId](#cfn-ssmcontacts-contactchannel-contactid): String
  [DeferActivation](#cfn-ssmcontacts-contactchannel-deferactivation): Boolean
```

## Properties<a name="aws-resource-ssmcontacts-contactchannel-properties"></a>

`ChannelAddress`  <a name="cfn-ssmcontacts-contactchannel-channeladdress"></a>
The details that Incident Manager uses when trying to engage the contact channel\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelName`  <a name="cfn-ssmcontacts-contactchannel-channelname"></a>
The name of the contact channel\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.\-]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelType`  <a name="cfn-ssmcontacts-contactchannel-channeltype"></a>
The type of the contact channel\. Incident Manager supports three contact methods:  
+ SMS
+ VOICE
+ EMAIL
*Required*: Yes  
*Type*: String  
*Allowed values*: `EMAIL | SMS | VOICE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContactId`  <a name="cfn-ssmcontacts-contactchannel-contactid"></a>
The Amazon Resource Name \(ARN\) of the contact you are adding the contact channel to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws|aws-cn|aws-us-gov):ssm-contacts:[-\w+=\/,.@]*:[0-9]+:([\w+=\/,.@:-]+)*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeferActivation`  <a name="cfn-ssmcontacts-contactchannel-deferactivation"></a>
If you want to activate the channel at a later time, you can choose to defer activation\. Incident Manager can't engage your contact channel until it has been activated\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssmcontacts-contactchannel-return-values"></a>

### Ref<a name="aws-resource-ssmcontacts-contactchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource, such as `arn:aws:ssm-contacts:us-west-2:123456789012:contact-channel/contactalias/cec1bb12-34f5-6789-a1ee-e1ca2345d6f7`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ssmcontacts-contactchannel-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ssmcontacts-contactchannel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `ContactChannel` resource\.