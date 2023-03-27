# AWS::ConnectCampaigns::Campaign OutboundCallConfig<a name="aws-properties-connectcampaigns-campaign-outboundcallconfig"></a>

Contains outbound call configuration for an outbound campaign\.

## Syntax<a name="aws-properties-connectcampaigns-campaign-outboundcallconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connectcampaigns-campaign-outboundcallconfig-syntax.json"></a>

```
{
  "[AnswerMachineDetectionConfig](#cfn-connectcampaigns-campaign-outboundcallconfig-answermachinedetectionconfig)" : AnswerMachineDetectionConfig,
  "[ConnectContactFlowArn](#cfn-connectcampaigns-campaign-outboundcallconfig-connectcontactflowarn)" : String,
  "[ConnectQueueArn](#cfn-connectcampaigns-campaign-outboundcallconfig-connectqueuearn)" : String,
  "[ConnectSourcePhoneNumber](#cfn-connectcampaigns-campaign-outboundcallconfig-connectsourcephonenumber)" : String
}
```

### YAML<a name="aws-properties-connectcampaigns-campaign-outboundcallconfig-syntax.yaml"></a>

```
  [AnswerMachineDetectionConfig](#cfn-connectcampaigns-campaign-outboundcallconfig-answermachinedetectionconfig): 
    AnswerMachineDetectionConfig
  [ConnectContactFlowArn](#cfn-connectcampaigns-campaign-outboundcallconfig-connectcontactflowarn): String
  [ConnectQueueArn](#cfn-connectcampaigns-campaign-outboundcallconfig-connectqueuearn): String
  [ConnectSourcePhoneNumber](#cfn-connectcampaigns-campaign-outboundcallconfig-connectsourcephonenumber): String
```

## Properties<a name="aws-properties-connectcampaigns-campaign-outboundcallconfig-properties"></a>

`AnswerMachineDetectionConfig`  <a name="cfn-connectcampaigns-campaign-outboundcallconfig-answermachinedetectionconfig"></a>
Whether answering machine detection has been enabled\.  
*Required*: No  
*Type*: [AnswerMachineDetectionConfig](aws-properties-connectcampaigns-campaign-answermachinedetectionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectContactFlowArn`  <a name="cfn-connectcampaigns-campaign-outboundcallconfig-connectcontactflowarn"></a>
The Amazon Resource Name \(ARN\) of the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectQueueArn`  <a name="cfn-connectcampaigns-campaign-outboundcallconfig-connectqueuearn"></a>
The Amazon Resource Name \(ARN\) of the queue\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectSourcePhoneNumber`  <a name="cfn-connectcampaigns-campaign-outboundcallconfig-connectsourcephonenumber"></a>
The phone number associated with the outbound call\. This is the caller ID that is displayed to customers when an agent calls them\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)