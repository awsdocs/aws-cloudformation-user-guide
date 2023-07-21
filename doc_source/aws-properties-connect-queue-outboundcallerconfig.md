# AWS::Connect::Queue OutboundCallerConfig<a name="aws-properties-connect-queue-outboundcallerconfig"></a>

The outbound caller ID name, number, and outbound whisper flow\.

## Syntax<a name="aws-properties-connect-queue-outboundcallerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-queue-outboundcallerconfig-syntax.json"></a>

```
{
  "[OutboundCallerIdName](#cfn-connect-queue-outboundcallerconfig-outboundcalleridname)" : String,
  "[OutboundCallerIdNumberArn](#cfn-connect-queue-outboundcallerconfig-outboundcalleridnumberarn)" : String,
  "[OutboundFlowArn](#cfn-connect-queue-outboundcallerconfig-outboundflowarn)" : String
}
```

### YAML<a name="aws-properties-connect-queue-outboundcallerconfig-syntax.yaml"></a>

```
  [OutboundCallerIdName](#cfn-connect-queue-outboundcallerconfig-outboundcalleridname): String
  [OutboundCallerIdNumberArn](#cfn-connect-queue-outboundcallerconfig-outboundcalleridnumberarn): String
  [OutboundFlowArn](#cfn-connect-queue-outboundcallerconfig-outboundflowarn): String
```

## Properties<a name="aws-properties-connect-queue-outboundcallerconfig-properties"></a>

`OutboundCallerIdName`  <a name="cfn-connect-queue-outboundcallerconfig-outboundcalleridname"></a>
The caller ID name\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutboundCallerIdNumberArn`  <a name="cfn-connect-queue-outboundcallerconfig-outboundcalleridnumberarn"></a>
The Amazon Resource Name \(ARN\) of the outbound caller ID number\.  
Only use the phone number ARN format that doesn't contain `instance` in the path, for example, `arn:aws:connect:us-east-1:1234567890:phone-number/uuid`\. This is the same ARN format that is returned when you create a phone number using CloudFormation, or when you call the [ListPhoneNumbersV2](https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html) API\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutboundFlowArn`  <a name="cfn-connect-queue-outboundcallerconfig-outboundflowarn"></a>
The Amazon Resource Name \(ARN\) of the outbound flow\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)