# AWS::MediaLive::Input<a name="aws-resource-medialive-input"></a>

The AWS::MediaLive::Input resource is a MediaLive resource type that creates an input\.

A MediaLive input holds information that describes how the MediaLive channel is connected to the upstream system that is providing the source content that is to be transcoded\. 

## Syntax<a name="aws-resource-medialive-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-medialive-input-syntax.json"></a>

```
{
  "Type" : "AWS::MediaLive::Input",
  "Properties" : {
      "[Destinations](#cfn-medialive-input-destinations)" : [ InputDestinationRequest, ... ],
      "[InputDevices](#cfn-medialive-input-inputdevices)" : [ InputDeviceSettings, ... ],
      "[InputSecurityGroups](#cfn-medialive-input-inputsecuritygroups)" : [ String, ... ],
      "[MediaConnectFlows](#cfn-medialive-input-mediaconnectflows)" : [ MediaConnectFlowRequest, ... ],
      "[Name](#cfn-medialive-input-name)" : String,
      "[RoleArn](#cfn-medialive-input-rolearn)" : String,
      "[Sources](#cfn-medialive-input-sources)" : [ InputSourceRequest, ... ],
      "[Tags](#cfn-medialive-input-tags)" : Json,
      "[Type](#cfn-medialive-input-type)" : String,
      "[Vpc](#cfn-medialive-input-vpc)" : InputVpcRequest
    }
}
```

### YAML<a name="aws-resource-medialive-input-syntax.yaml"></a>

```
Type: AWS::MediaLive::Input
Properties: 
  [Destinations](#cfn-medialive-input-destinations): 
    - InputDestinationRequest
  [InputDevices](#cfn-medialive-input-inputdevices): 
    - InputDeviceSettings
  [InputSecurityGroups](#cfn-medialive-input-inputsecuritygroups): 
    - String
  [MediaConnectFlows](#cfn-medialive-input-mediaconnectflows): 
    - MediaConnectFlowRequest
  [Name](#cfn-medialive-input-name): String
  [RoleArn](#cfn-medialive-input-rolearn): String
  [Sources](#cfn-medialive-input-sources): 
    - InputSourceRequest
  [Tags](#cfn-medialive-input-tags): Json
  [Type](#cfn-medialive-input-type): String
  [Vpc](#cfn-medialive-input-vpc): 
    InputVpcRequest
```

## Properties<a name="aws-resource-medialive-input-properties"></a>

`Destinations`  <a name="cfn-medialive-input-destinations"></a>
Read\-only\. Specifies the URLs for a push input\. The input is pushing to these addresses in order to deliver to MediaLive\. You don't set these values\.  
*Required*: No  
*Type*: List of [InputDestinationRequest](aws-properties-medialive-input-inputdestinationrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputDevices`  <a name="cfn-medialive-input-inputdevices"></a>
Include this element only for an INPUT\_DEVICE type of input\. Settings for the devices\.  
*Required*: No  
*Type*: List of [InputDeviceSettings](aws-properties-medialive-input-inputdevicesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSecurityGroups`  <a name="cfn-medialive-input-inputsecuritygroups"></a>
A list of security groups referenced by IDs to attach to the input\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaConnectFlows`  <a name="cfn-medialive-input-mediaconnectflows"></a>
Include this element only for a MEDIACONNECT type of input\. A list of the MediaConnect Flows that you want to use in this input\. You can specify as few as one Flow and presently, as many as two\. The only requirement is when you have more than one is that each Flow is in a separate Availability Zone as this ensures your EML input is redundant to AZ issues\.  
*Required*: No  
*Type*: List of [MediaConnectFlowRequest](aws-properties-medialive-input-mediaconnectflowrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-input-name"></a>
Name of the input\. Required\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-medialive-input-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role this input assumes during and after creation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sources`  <a name="cfn-medialive-input-sources"></a>
Include this element only if the input is a pull input\. Specifies the source URLs for the input\.  
*Required*: No  
*Type*: List of [InputSourceRequest](aws-properties-medialive-input-inputsourcerequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-medialive-input-tags"></a>
A collection of key\-value pairs\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-medialive-input-type"></a>
You must include this element\. It sets the type of the input, which then determines which other elements you must include in this CreateInput element\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Vpc`  <a name="cfn-medialive-input-vpc"></a>
Include this element only for a VPC type of input\.  
*Required*: No  
*Type*: [InputVpcRequest](aws-properties-medialive-input-inputvpcrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-medialive-input-return-values"></a>

### Ref<a name="aws-resource-medialive-input-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the input\.

For example: `{ "Ref": "1234567" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-medialive-input-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

The IP addresses are in a string format that shows a list\. For example `[rtp://203.0.113.28:5000, rtp://203.0.113.33:5005]`

#### <a name="aws-resource-medialive-input-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the MediaLive input\. For example: arn:aws:medialive:us\-west\-1:111122223333:medialive:input:1234567\. MediaLive creates this ARN when it creates the input\. 

`Destinations`  <a name="Destinations-fn::getatt"></a>
For a push input, the destination or destinations for the input\. The destinations are the IP addresses on MediaLive where the upstream system pushes the content for this input\. MediaLive creates these IP addresses when it creates the input\. 

`Sources`  <a name="Sources-fn::getatt"></a>
For a pull input, the source or sources for the input\. The sources are the IP addresses on the upstream system where MediaLive pulls the content from for this input\. You included these IP addresses in the create request\.