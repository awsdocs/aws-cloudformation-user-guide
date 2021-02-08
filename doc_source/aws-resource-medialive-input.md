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
The destination settings for push types of inputs\. If the input is a pull type, these settings don't apply\.   
*Required*: No  
*Type*: List of [InputDestinationRequest](aws-properties-medialive-input-inputdestinationrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputDevices`  <a name="cfn-medialive-input-inputdevices"></a>
Settings for the devices\.  
*Required*: No  
*Type*: List of [InputDeviceSettings](aws-properties-medialive-input-inputdevicesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSecurityGroups`  <a name="cfn-medialive-input-inputsecuritygroups"></a>
The list of input security groups \(referenced by IDs\) to attach to the input if the input is a push type\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaConnectFlows`  <a name="cfn-medialive-input-mediaconnectflows"></a>
Settings that apply only if the input is a MediaConnect input\.  
*Required*: No  
*Type*: List of [MediaConnectFlowRequest](aws-properties-medialive-input-mediaconnectflowrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-input-name"></a>
A name for the input\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-medialive-input-rolearn"></a>
The IAM role for MediaLive to assume when creating a MediaConnect input or Amazon VPC input\. This doesn't apply to other types of inputs\. The role is identified by its ARN\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sources`  <a name="cfn-medialive-input-sources"></a>
The source settings for a pull type of input\. These settings don't apply if the input is a push type\.   
*Required*: No  
*Type*: List of [InputSourceRequest](aws-properties-medialive-input-inputsourcerequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-medialive-input-tags"></a>
A collection of tags for this input\. Each tag is a key\-value pair\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-medialive-input-type"></a>
The type for this input\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Vpc`  <a name="cfn-medialive-input-vpc"></a>
Settings that apply only if the input is an Amazon VPC input\.   
*Required*: No  
*Type*: [InputVpcRequest](aws-properties-medialive-input-inputvpcrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-medialive-input-return-values"></a>

### Ref<a name="aws-resource-medialive-input-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the input\.

For example: `{ "Ref": "myInput" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-medialive-input-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-medialive-input-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the MediaLive input\. For example: arn:aws:medialive:us\-west\-1:111122223333:medialive:input:1234567\. MediaLive creates this ARN when it creates the input\. 

`Destinations`  <a name="Destinations-fn::getatt"></a>
For a push input, the destination or destinations for the input\. The destinations are the IP addresses on MediaLive where the upstream system pushes the content to for this input\. MediaLive creates these IP addresses when it creates the input\. 

`Sources`  <a name="Sources-fn::getatt"></a>
For a pull input, the source or sources for the input\. The sources are the IP addresses on the upstream system where MediaLive pulls the content from for this input\. You included these IP addresses in the create request\.