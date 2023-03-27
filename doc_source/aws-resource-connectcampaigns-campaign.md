# AWS::ConnectCampaigns::Campaign<a name="aws-resource-connectcampaigns-campaign"></a>

Contains information about an outbound campaign\.

## Syntax<a name="aws-resource-connectcampaigns-campaign-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connectcampaigns-campaign-syntax.json"></a>

```
{
  "Type" : "AWS::ConnectCampaigns::Campaign",
  "Properties" : {
      "[ConnectInstanceArn](#cfn-connectcampaigns-campaign-connectinstancearn)" : String,
      "[DialerConfig](#cfn-connectcampaigns-campaign-dialerconfig)" : DialerConfig,
      "[Name](#cfn-connectcampaigns-campaign-name)" : String,
      "[OutboundCallConfig](#cfn-connectcampaigns-campaign-outboundcallconfig)" : OutboundCallConfig,
      "[Tags](#cfn-connectcampaigns-campaign-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connectcampaigns-campaign-syntax.yaml"></a>

```
Type: AWS::ConnectCampaigns::Campaign
Properties: 
  [ConnectInstanceArn](#cfn-connectcampaigns-campaign-connectinstancearn): String
  [DialerConfig](#cfn-connectcampaigns-campaign-dialerconfig): 
    DialerConfig
  [Name](#cfn-connectcampaigns-campaign-name): String
  [OutboundCallConfig](#cfn-connectcampaigns-campaign-outboundcallconfig): 
    OutboundCallConfig
  [Tags](#cfn-connectcampaigns-campaign-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connectcampaigns-campaign-properties"></a>

`ConnectInstanceArn`  <a name="cfn-connectcampaigns-campaign-connectinstancearn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Connect instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DialerConfig`  <a name="cfn-connectcampaigns-campaign-dialerconfig"></a>
Contains information about the dialer configuration\.  
*Required*: Yes  
*Type*: [DialerConfig](aws-properties-connectcampaigns-campaign-dialerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connectcampaigns-campaign-name"></a>
The name of the campaign\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutboundCallConfig`  <a name="cfn-connectcampaigns-campaign-outboundcallconfig"></a>
Contains information about the outbound call configuration\.  
*Required*: Yes  
*Type*: [OutboundCallConfig](aws-properties-connectcampaigns-campaign-outboundcallconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connectcampaigns-campaign-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connectcampaigns-campaign-return-values"></a>

### Ref<a name="aws-resource-connectcampaigns-campaign-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the campaign name\. For example:

`{ "Ref": "myCampaignName" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connectcampaigns-campaign-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connectcampaigns-campaign-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the high\-volume outbound campaign\.