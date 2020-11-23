# AWS::PinpointEmail::ConfigurationSetEventDestination PinpointDestination<a name="aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination"></a>

An object that defines a Amazon Pinpoint destination for email events\. You can use Amazon Pinpoint events to create attributes in Amazon Pinpoint projects\. You can use these attributes to create segments for your campaigns\.

## Syntax<a name="aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination-syntax.json"></a>

```
{
  "[ApplicationArn](#cfn-pinpointemail-configurationseteventdestination-pinpointdestination-applicationarn)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination-syntax.yaml"></a>

```
  [ApplicationArn](#cfn-pinpointemail-configurationseteventdestination-pinpointdestination-applicationarn): String
```

## Properties<a name="aws-properties-pinpointemail-configurationseteventdestination-pinpointdestination-properties"></a>

`ApplicationArn`  <a name="cfn-pinpointemail-configurationseteventdestination-pinpointdestination-applicationarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Pinpoint project that you want to send email events to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)