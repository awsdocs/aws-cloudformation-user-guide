# AWS::MediaConnect::BridgeSource BridgeFlowSource<a name="aws-properties-mediaconnect-bridgesource-bridgeflowsource"></a>

The source of the bridge\. A flow source originates in MediaConnect as an existing cloud flow\. 

## Syntax<a name="aws-properties-mediaconnect-bridgesource-bridgeflowsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridgesource-bridgeflowsource-syntax.json"></a>

```
{
  "[FlowArn](#cfn-mediaconnect-bridgesource-bridgeflowsource-flowarn)" : String,
  "[FlowVpcInterfaceAttachment](#cfn-mediaconnect-bridgesource-bridgeflowsource-flowvpcinterfaceattachment)" : VpcInterfaceAttachment
}
```

### YAML<a name="aws-properties-mediaconnect-bridgesource-bridgeflowsource-syntax.yaml"></a>

```
  [FlowArn](#cfn-mediaconnect-bridgesource-bridgeflowsource-flowarn): String
  [FlowVpcInterfaceAttachment](#cfn-mediaconnect-bridgesource-bridgeflowsource-flowvpcinterfaceattachment): 
    VpcInterfaceAttachment
```

## Properties<a name="aws-properties-mediaconnect-bridgesource-bridgeflowsource-properties"></a>

`FlowArn`  <a name="cfn-mediaconnect-bridgesource-bridgeflowsource-flowarn"></a>
The ARN of the cloud flow used as a source of this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowVpcInterfaceAttachment`  <a name="cfn-mediaconnect-bridgesource-bridgeflowsource-flowvpcinterfaceattachment"></a>
The name of the VPC interface attachment to use for this source\.  
*Required*: No  
*Type*: [VpcInterfaceAttachment](aws-properties-mediaconnect-bridgesource-vpcinterfaceattachment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)