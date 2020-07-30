# AWS::PinpointEmail::ConfigurationSetEventDestination<a name="aws-resource-pinpointemail-configurationseteventdestination"></a>

Create an event destination\. In Amazon Pinpoint, *events* include message sends, deliveries, opens, clicks, bounces, and complaints\. *Event destinations* are places that you can send information about these events to\. For example, you can send event data to Amazon SNS to receive notifications when you receive bounces or complaints, or you can use Amazon Kinesis Data Firehose to stream data to Amazon S3 for long\-term storage\.

A single configuration set can include more than one event destination\.

## Syntax<a name="aws-resource-pinpointemail-configurationseteventdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpointemail-configurationseteventdestination-syntax.json"></a>

```
{
  "Type" : "AWS::PinpointEmail::ConfigurationSetEventDestination",
  "Properties" : {
      "[ConfigurationSetName](#cfn-pinpointemail-configurationseteventdestination-configurationsetname)" : String,
      "[EventDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination)" : EventDestination,
      "[EventDestinationName](#cfn-pinpointemail-configurationseteventdestination-eventdestinationname)" : String
    }
}
```

### YAML<a name="aws-resource-pinpointemail-configurationseteventdestination-syntax.yaml"></a>

```
Type: AWS::PinpointEmail::ConfigurationSetEventDestination
Properties: 
  [ConfigurationSetName](#cfn-pinpointemail-configurationseteventdestination-configurationsetname): String
  [EventDestination](#cfn-pinpointemail-configurationseteventdestination-eventdestination): 
    EventDestination
  [EventDestinationName](#cfn-pinpointemail-configurationseteventdestination-eventdestinationname): String
```

## Properties<a name="aws-resource-pinpointemail-configurationseteventdestination-properties"></a>

`ConfigurationSetName`  <a name="cfn-pinpointemail-configurationseteventdestination-configurationsetname"></a>
The name of the configuration set that contains the event destination that you want to modify\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventDestination`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestination"></a>
An object that defines the event destination\.  
*Required*: No  
*Type*: [EventDestination](aws-properties-pinpointemail-configurationseteventdestination-eventdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventDestinationName`  <a name="cfn-pinpointemail-configurationseteventdestination-eventdestinationname"></a>
The name of the event destination that you want to modify\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-pinpointemail-configurationseteventdestination-return-values"></a>

### Ref<a name="aws-resource-pinpointemail-configurationseteventdestination-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myEventDestination" }` 

For the Amazon Pinpoint event destination `myEventDestination`, Ref returns the name of the configuration set event destination\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.