# AWS::Events::EventBusPolicy Condition<a name="aws-properties-events-eventbuspolicy-condition"></a>

A JSON string which you can use to limit the event bus permissions you are granting to only accounts that fulfill the condition\. Currently, the only supported condition is membership in a certain AWS organization\. The string must contain `Type`, `Key`, and `Value` fields\. The `Value` field specifies the ID of the AWS organization\. Following is an example value for `Condition`:

 `'{"Type" : "StringEquals", "Key": "aws:PrincipalOrgID", "Value": "o-1234567890"}'` 

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
Specifies the key for the condition\. Currently the only supported key is `aws:PrincipalOrgID`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-events-eventbuspolicy-condition-type"></a>
Specifies the type of condition\. Currently the only supported value is `StringEquals`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-events-eventbuspolicy-condition-value"></a>
Specifies the value for the key\. Currently, this must be the ID of the organization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)