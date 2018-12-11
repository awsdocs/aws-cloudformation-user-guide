# AWS::Events::EventBusPolicy<a name="aws-resource-events-eventbuspolicy"></a>

The `AWS::Events::EventBusPolicy` resource creates an event bus policy for Amazon CloudWatch Events\. An event bus policy enables your account to receive events from other AWS accounts\. These events can trigger CloudWatch Events rules created in your account\. For more information, see [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/CloudWatchEvents-CrossAccountEventDelivery.html) in the *Amazon CloudWatch Events User Guide*\. 

**Note**  
If you grant permission to other accounts using *Condition* and specifying an organization, then accounts in that organization must specify a `RoleArn` with proper permissions when they use `PutTarget` to add your account's event bus as a target\.

## Syntax<a name="aws-resource-events-eventbuspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-eventbuspolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Events::EventBusPolicy",
  "Properties" : {
    "[Action](#cfn-events-eventbuspolicy-action)" : String,
    "[Condition](#cfn-events-eventbuspolicy-condition)" : [*Condition*](aws-properties-events-eventbuspolicy-condition.md),
    "[Principal](#cfn-events-eventbuspolicy-principal)" : String,
    "[StatementId](#cfn-events-eventbuspolicy-statementid)" : String
  }
}
```

### YAML<a name="aws-resource-events-eventbuspolicy-syntax.yaml"></a>

```
Type: "AWS::Events::EventBusPolicy"
Properties:
  [Action](#cfn-events-eventbuspolicy-action): String
  [Condition](#cfn-events-eventbuspolicy-condition): [*Condition*](aws-properties-events-eventbuspolicy-condition.md)
  [Principal](#cfn-events-eventbuspolicy-principal): String
  [StatementId](#cfn-events-eventbuspolicy-statementid): String
```

## Properties<a name="aws-resource-events-eventbuspolicy-properties"></a>

`Action`  <a name="cfn-events-eventbuspolicy-action"></a>
The action that you are enabling the other account to perform\. Currently, this must be `events:PutEvents`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Condition`  <a name="cfn-events-eventbuspolicy-condition"></a>
A JSON string which you can use to limit the event bus permissions you are granting to only accounts that fulfill the condition\. Currently, the only supported condition is membership in a certain AWS organization\. The string must contain `Type`, `Key`, and `Value` fields\.  
Currently, the `Type` must be `StringEquals`, the `Key` must be `aws:PrincipalOrgID`, and the `Value` field specifies the ID of the AWS organization\.  
If you specify `Condition` with an AWS organization ID, you must specify "\*" as the value for `Principal`\. This grants permission to all the accounts in the named organization\.  
 *Required*: No  
 *Type*: [Condition](aws-properties-events-eventbuspolicy-condition.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Principal`  <a name="cfn-events-eventbuspolicy-principal"></a>
The 12\-digit AWS account ID that you are permitting to put events to your default event bus\. Specify `*` to permit any account to put events to your default event bus, or if you are specifying an organization ID in the `Condition` object\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StatementId`  <a name="cfn-events-eventbuspolicy-statementid"></a>
An identifier string for the external account to which you are granting permissions\. To later revoke the permission for this external account, you need to know this string\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-events-eventbuspolicy-returnvalues"></a>

### Ref<a name="aws-resource-events-eventbuspolicy-ref"></a>

When you pass the logical ID of an `AWS::Events::EventBusPolicy` resource to the intrinsic `Ref` function, the function returns the event bus policy ID, such as `EventBusPolicy-1aBCdeFGh2J3`\. 

For more information, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-events-eventbuspolicy-examples"></a>

### Grant Permission to One Account<a name="aws-resource-events-eventbuspolicy-example1"></a>

The following example grants permission to one AWS account with an account ID of `111122223333`\.

#### JSON<a name="aws-resource-events-eventbuspolicy-example1.json"></a>

```
"SampleEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "Action": "events:PutEvents",
        "Principal": "111122223333",
        "StatementId": "MyStatement"
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy-example1.yaml"></a>

```
SampleEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy,
    Properties: 
        Action: "events:PutEvents"
        Principal: "111122223333"
        StatementId: "MyStatement"
```

### Grant Permission to an Organization<a name="aws-resource-events-eventbuspolicy-example2"></a>

The following example grants permission to all AWS accounts in the organization with an organization ID of `o-1234567890`\.

#### JSON<a name="aws-resource-events-eventbuspolicy-example2.json"></a>

```
"SampleEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "Action": "events:PutEvents",
        "Principal": "*",
        "StatementId": "MyStatement",
        "Condition": {
            "Type": "StringEquals",
            "Key": "aws:PrincipalOrgID",
            "Value": "o-1234567890"
        }
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy-example2.yaml"></a>

```
SampleEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy,
    Properties: 
        Action: "events:PutEvents"
        Principal: "*"
        StatementId: "MyStatement"
        Condition: 
            Type: "StringEquals",
            Key: "aws:PrincipalOrgID",
            Value: "o-1234567890"
```

## See Also<a name="aws-resource-events-eventbuspolicy-seealso"></a>
+ [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/CloudWatchEvents-CrossAccountEventDelivery.html) in the *Amazon CloudWatch User Guide*
+ [PutPermission](https://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutPermission.html) in the *Amazon CloudWatch API Reference*