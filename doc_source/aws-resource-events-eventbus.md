# AWS::Events::EventBus<a name="aws-resource-events-eventbus"></a>

Creates a new event bus within your account\. This can be a custom event bus which you can use to receive events from your custom applications and services, or it can be a partner event bus which can be matched to a partner event source\.

## Syntax<a name="aws-resource-events-eventbus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-eventbus-syntax.json"></a>

```
{
  "Type" : "AWS::Events::EventBus",
  "Properties" : {
      "[EventSourceName](#cfn-events-eventbus-eventsourcename)" : String,
      "[Name](#cfn-events-eventbus-name)" : String,
      "[Tags](#cfn-events-eventbus-tags)" : [ TagEntry, ... ]
    }
}
```

### YAML<a name="aws-resource-events-eventbus-syntax.yaml"></a>

```
Type: AWS::Events::EventBus
Properties: 
  [EventSourceName](#cfn-events-eventbus-eventsourcename): String
  [Name](#cfn-events-eventbus-name): String
  [Tags](#cfn-events-eventbus-tags): 
    - TagEntry
```

## Properties<a name="aws-resource-events-eventbus-properties"></a>

`EventSourceName`  <a name="cfn-events-eventbus-eventsourcename"></a>
If you are creating a partner event bus, this specifies the partner event source that the new event bus will be matched with\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `aws\.partner(/[\.\-_A-Za-z0-9]+){2,}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-events-eventbus-name"></a>
The name of the new event bus\.   
Custom event bus names can't contain the `/` character, but you can use the `/` character in partner event bus names\. In addition, for partner event buses, the name must exactly match the name of the partner event source that this event bus is matched to\.  
You can't use the name `default` for a custom event bus, as this name is already used for your account's default event bus\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[/\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-events-eventbus-tags"></a>
Tags to associate with the event bus\.  
*Required*: No  
*Type*: List of [TagEntry](aws-properties-events-eventbus-tagentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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

The following example creates a partner event bus named `aws.partner.repo1`\. 

#### JSON<a name="aws-resource-events-eventbus--examples--Create_a_partner_event_bus--json"></a>

```
"SamplePartnerEventBus": {
    "Type": "AWS::Events::EventBus",
    "Properties": {
        "EventSourceName": "aws.partner/PartnerName/acct1/repo1",
        "Name": "aws.partner.repo1"
    }
}
```

#### YAML<a name="aws-resource-events-eventbus--examples--Create_a_partner_event_bus--yaml"></a>

```
SamplePartnerEventBus: 
    Type: AWS::Events::EventBus
    Properties: 
        EventSourceName: "aws.partner/PartnerName/acct1/repo1"
        Name: "aws.partner.repo1"
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