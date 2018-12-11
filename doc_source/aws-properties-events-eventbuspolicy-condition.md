# Amazon CloudWatch Events EventBusPolicy Condition<a name="aws-properties-events-eventbuspolicy-condition"></a>

<a name="aws-properties-events-eventbuspolicy-condition-description"></a>The `Condition` property type enables you to grant event bus permissions to all the AWS accounts in an organization\.

<a name="aws-properties-events-eventbuspolicy-condition-inheritance"></a> `Condition` is a property of the [AWS::Events::EventBusPolicy](aws-resource-events-eventbuspolicy.md) resource type\.

## Syntax<a name="aws-properties-events-eventbuspolicy-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-eventbuspolicy-condition-syntax.json"></a>

```
{
  "[Key](#cfn-events-eventbuspolicy-condition-key)" : String,
  "[Type](#cfn-events-eventbuspolicy-condition-type)" : String,
  "[Value](#cfn-events-eventbuspolicy-condition-value)" : String
}
```

### YAML<a name="aws-properties-events-eventbuspolicy-condition-syntax.yaml"></a>

```
[Key](#cfn-events-eventbuspolicy-condition-key): String
[Type](#cfn-events-eventbuspolicy-condition-type): String
[Value](#cfn-events-eventbuspolicy-condition-value): String
```

## Properties<a name="aws-properties-events-eventbuspolicy-condition-properties"></a>

`Key`  <a name="cfn-events-eventbuspolicy-condition-key"></a>
Currently, `Key` must be `aws:PrincipalOrgID`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Type`  <a name="cfn-events-eventbuspolicy-condition-type"></a>
Currently, `Type` must be `StringEquals`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-events-eventbuspolicy-condition-value"></a>
Specifies the ID of the AWS organization to which you want to grant permission\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-events-eventbuspolicy-condition-seealso"></a>
+ [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/CloudWatchEvents-CrossAccountEventDelivery.html) in the *Amazon CloudWatch Events User Guide*
+ [PutPermission](https://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutPermission.html) in the *Amazon CloudWatch Events API Reference*