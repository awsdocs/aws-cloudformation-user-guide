# AWS::MediaConnect::Bridge BridgeFlowSource<a name="aws-properties-mediaconnect-bridge-bridgeflowsource"></a>

The source of the bridge\. A flow source originates in MediaConnect as an existing cloud flow\. 

## Syntax<a name="aws-properties-mediaconnect-bridge-bridgeflowsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-bridgeflowsource-syntax.json"></a>

```
{
  "[FlowArn](#cfn-mediaconnect-bridge-bridgeflowsource-flowarn)" : String,
  "[FlowVpcInterfaceAttachment](#cfn-mediaconnect-bridge-bridgeflowsource-flowvpcinterfaceattachment)" : VpcInterfaceAttachment,
  "[Name](#cfn-mediaconnect-bridge-bridgeflowsource-name)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-bridgeflowsource-syntax.yaml"></a>

```
  [FlowArn](#cfn-mediaconnect-bridge-bridgeflowsource-flowarn): String
  [FlowVpcInterfaceAttachment](#cfn-mediaconnect-bridge-bridgeflowsource-flowvpcinterfaceattachment): 
    VpcInterfaceAttachment
  [Name](#cfn-mediaconnect-bridge-bridgeflowsource-name): String
```

## Properties<a name="aws-properties-mediaconnect-bridge-bridgeflowsource-properties"></a>

`FlowArn`  <a name="cfn-mediaconnect-bridge-bridgeflowsource-flowarn"></a>
The ARN of the cloud flow used as a source of this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowVpcInterfaceAttachment`  <a name="cfn-mediaconnect-bridge-bridgeflowsource-flowvpcinterfaceattachment"></a>
The name of the VPC interface attachment to use for this source\.  
*Required*: No  
*Type*: [VpcInterfaceAttachment](aws-properties-mediaconnect-bridge-vpcinterfaceattachment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-bridge-bridgeflowsource-name"></a>
The name of the flow source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)