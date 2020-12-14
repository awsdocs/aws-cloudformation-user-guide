# AWS::Events::EventBus<a name="aws-resource-events-eventbus"></a>

The `AWS::Events::EventBus` resource creates or updates a partner event bus or custom event bus\. Partner event buses can receive events from applications and services created by AWS SaaS partners\. You need to create a partner event bus for each partner event source that you want to receive events from\. 

Custom event buses can receive events from your own custom applications\.

To review the limit for how many rules each event bus may have, see [Service Limits](https://docs.aws.amazon.com/eventbridge/latest/userguide/cloudwatch-limits-eventbridge.html)\.

## Syntax<a name="aws-resource-events-eventbus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-eventbus-syntax.json"></a>

```
{
  "Type" : "AWS::Events::EventBus",
  "Properties" : {
      "[EventSourceName](#cfn-events-eventbus-eventsourcename)" : String,
      "[Name](#cfn-events-eventbus-name)" : String
    }
}
```

### YAML<a name="aws-resource-events-eventbus-syntax.yaml"></a>

```
Type: AWS::Events::EventBus
Properties: 
  [EventSourceName](#cfn-events-eventbus-eventsourcename): String
  [Name](#cfn-events-eventbus-name): String
```

## Properties<a name="aws-resource-events-eventbus-properties"></a>

`EventSourceName`  <a name="cfn-events-eventbus-eventsourcename"></a>
The name of the partner event source to associate with this event bus, if you are creating a partner event bus\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-events-eventbus-name"></a>
The name of the event bus you are creating\. The names of custom event buses can't contain the `/` character\. You can't use the name `default` for a custom event bus\.  
If you are creating a partner event bus, this name must exactly match the name of the partner event source that this bus is matched to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-events-eventbus-return-values"></a>

### Ref<a name="aws-resource-events-eventbus-return-values-ref"></a>

The name of the new event bus\.

### Fn::GetAtt<a name="aws-resource-events-eventbus-return-values-fn--getatt"></a>

The ARN of the task definition to use\. If no task revision is supplied, it defaults to the most recent revision at the time of resource creation\.

#### <a name="aws-resource-events-eventbus-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the event bus, such as `arn:aws:events:us-east-2:123456789012:event-bus/aws.partner/PartnerName/acct1/repo1`\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the event bus, such as `PartnerName/acct1/repo1`\.

`Policy`  <a name="Policy-fn::getatt"></a>
The policy for the event bus in JSON form\.

## Examples<a name="aws-resource-events-eventbus--examples"></a>



### Create a partner event bus<a name="aws-resource-events-eventbus--examples--Create_a_partner_event_bus"></a>

The following example creates a partner event bus named `aws.partner/PartnerName/acct1/repo1`\. 

#### JSON<a name="aws-resource-events-eventbus--examples--Create_a_partner_event_bus--json"></a>

```
"SamplePartnerEventBus": {
    "Type": "AWS::Events::EventBus",
    "Properties": {
        "EventSourceName": "aws.partner/PartnerName/acct1/repo1",
        "Name": "aws.partner/PartnerName/acct1/repo1"
    }
}
```

#### YAML<a name="aws-resource-events-eventbus--examples--Create_a_partner_event_bus--yaml"></a>

```
SamplePartnerEventBus: 
    Type: AWS::Events::EventBus
    Properties: 
        EventSourceName: "aws.partner/PartnerName/acct1/repo1"
        Name: "aws.partner/PartnerName/acct1/repo1"
```

### Create a custom event bus<a name="aws-resource-events-eventbus--examples--Create_a_custom_event_bus"></a>

The following example creates a custom event bus named `MyCustomEventBus`\.

#### JSON<a name="aws-resource-events-eventbus--examples--Create_a_custom_event_bus--json"></a>

```
"SampleCustomEventBus": {
    "Type": "AWS::Events::EventBus",
    "Properties": {
        "Name": "MyCustomEventBus"
    }
}
```

#### YAML<a name="aws-resource-events-eventbus--examples--Create_a_custom_event_bus--yaml"></a>

```
SampleCustomEventBus: 
    Type: AWS::Events::EventBus
    Properties: 
        Name: "MyCustomEventBus"
```