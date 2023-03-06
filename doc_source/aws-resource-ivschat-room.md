# AWS::IVSChat::Room<a name="aws-resource-ivschat-room"></a>

The `AWS::IVSChat::Room` resource specifies an Amazon IVS room that allows clients to connect and pass messages\. For more information, see [CreateRoom](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_CreateRoom.html) in the *Amazon Interactive Video Service Chat API Reference*\.

## Syntax<a name="aws-resource-ivschat-room-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ivschat-room-syntax.json"></a>

```
{
  "Type" : "AWS::IVSChat::Room",
  "Properties" : {
      "[LoggingConfigurationIdentifiers](#cfn-ivschat-room-loggingconfigurationidentifiers)" : [ String, ... ],
      "[MaximumMessageLength](#cfn-ivschat-room-maximummessagelength)" : Integer,
      "[MaximumMessageRatePerSecond](#cfn-ivschat-room-maximummessageratepersecond)" : Integer,
      "[MessageReviewHandler](#cfn-ivschat-room-messagereviewhandler)" : MessageReviewHandler,
      "[Name](#cfn-ivschat-room-name)" : String,
      "[Tags](#cfn-ivschat-room-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ivschat-room-syntax.yaml"></a>

```
Type: AWS::IVSChat::Room
Properties: 
  [LoggingConfigurationIdentifiers](#cfn-ivschat-room-loggingconfigurationidentifiers): 
    - String
  [MaximumMessageLength](#cfn-ivschat-room-maximummessagelength): Integer
  [MaximumMessageRatePerSecond](#cfn-ivschat-room-maximummessageratepersecond): Integer
  [MessageReviewHandler](#cfn-ivschat-room-messagereviewhandler): 
    MessageReviewHandler
  [Name](#cfn-ivschat-room-name): String
  [Tags](#cfn-ivschat-room-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ivschat-room-properties"></a>

`LoggingConfigurationIdentifiers`  <a name="cfn-ivschat-room-loggingconfigurationidentifiers"></a>
List of logging\-configuration identifiers attached to the room\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumMessageLength`  <a name="cfn-ivschat-room-maximummessagelength"></a>
Maximum number of characters in a single message\. Messages are expected to be UTF\-8 encoded and this limit applies specifically to rune/code\-point count, not number of bytes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumMessageRatePerSecond`  <a name="cfn-ivschat-room-maximummessageratepersecond"></a>
Maximum number of messages per second that can be sent to the room \(by all clients\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageReviewHandler`  <a name="cfn-ivschat-room-messagereviewhandler"></a>
Configuration information for optional review of messages\.  
*Required*: No  
*Type*: [MessageReviewHandler](aws-properties-ivschat-room-messagereviewhandler.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ivschat-room-name"></a>
Room name\. The value does not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ivschat-room-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ivschat-room-return-values"></a>

### Ref<a name="aws-resource-ivschat-room-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the room ARN\. For example:

 `{ "Ref": "myRoom" }` 

For the Amazon IVS room `myRoom `, `Ref` returns the room ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ivschat-room-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ivschat-room-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The room ARN\. For example: `arn:aws:ivschat:us-west-2:123456789012:room/abcdABCDefgh`

`Id`  <a name="Id-fn::getatt"></a>
The room ID\. For example: `abcdABCDefgh`

## Examples<a name="aws-resource-ivschat-room--examples"></a>



### Room Template Examples<a name="aws-resource-ivschat-room--examples--Room_Template_Examples"></a>

The following examples specify an Amazon IVS Chat Room\.

#### JSON<a name="aws-resource-ivschat-room--examples--Room_Template_Examples--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "Room": {
      "Type": "AWS::IVSChat::Room",
      "Properties": {
        "Name": "MyRoom",
        "Tags": [
          { "Key": "MyKey", "Value": "MyValue" }
        ]
      }
    }
  },
  "Outputs": {
    "RoomArn": {
      "Value": { "Ref": "Room" }
    },
    "RoomId": {
      "Value": {
        "Fn::GetAtt": [
          "Room",
          "Id"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ivschat-room--examples--Room_Template_Examples--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  Room:
    Type: AWS::IVSChat::Room
    Properties:
      Name: MyRoom
      Tags:
        - Key: MyKey
          Value: MyValue
Outputs:
  RoomArn:
    Value: !Ref Room
  RoomId:
    Value: !GetAtt Room.Id
```

## See also<a name="aws-resource-ivschat-room--seealso"></a>
+ [Getting Started with Amazon Interactive Video Service](https://docs.aws.amazon.com/ivs/latest/userguide/getting-started.html)
+ [RoomSummary](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_RoomSummary.html) API data type
+ [CreateRoom](https://docs.aws.amazon.com/ivs/latest/ChatAPIReference/API_CreateRoom.html) API endpoint