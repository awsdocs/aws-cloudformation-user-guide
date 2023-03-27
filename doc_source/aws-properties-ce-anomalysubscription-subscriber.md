# AWS::CE::AnomalySubscription Subscriber<a name="aws-properties-ce-anomalysubscription-subscriber"></a>

The recipient of `AnomalySubscription` notifications\. 

## Syntax<a name="aws-properties-ce-anomalysubscription-subscriber-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ce-anomalysubscription-subscriber-syntax.json"></a>

```
{
  "[Address](#cfn-ce-anomalysubscription-subscriber-address)" : String,
  "[Status](#cfn-ce-anomalysubscription-subscriber-status)" : String,
  "[Type](#cfn-ce-anomalysubscription-subscriber-type)" : String
}
```

### YAML<a name="aws-properties-ce-anomalysubscription-subscriber-syntax.yaml"></a>

```
  [Address](#cfn-ce-anomalysubscription-subscriber-address): String
  [Status](#cfn-ce-anomalysubscription-subscriber-status): String
  [Type](#cfn-ce-anomalysubscription-subscriber-type): String
```

## Properties<a name="aws-properties-ce-anomalysubscription-subscriber-properties"></a>

`Address`  <a name="cfn-ce-anomalysubscription-subscriber-address"></a>
 The email address or SNS Topic Amazon Resource Name \(ARN\), depending on the `Type`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `302`  
*Pattern*: `(^[a-zA-Z0-9.!#$%&'*+=?^_‘{|}~-]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$)|(^arn:(aws[a-zA-Z-]*):sns:[a-zA-Z0-9-]+:[0-9]{12}:[a-zA-Z0-9_-]+(\.fifo)?$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-ce-anomalysubscription-subscriber-status"></a>
Indicates if the subscriber accepts the notifications\.   
*Required*: No  
*Type*: String  
*Allowed values*: `CONFIRMED | DECLINED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ce-anomalysubscription-subscriber-type"></a>
The notification delivery channel\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `EMAIL | SNS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)