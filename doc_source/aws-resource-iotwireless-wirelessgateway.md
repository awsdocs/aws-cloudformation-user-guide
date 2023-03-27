# AWS::IoTWireless::WirelessGateway<a name="aws-resource-iotwireless-wirelessgateway"></a>

Provisions a wireless gateway\.

## Syntax<a name="aws-resource-iotwireless-wirelessgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-wirelessgateway-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::WirelessGateway",
  "Properties" : {
      "[Description](#cfn-iotwireless-wirelessgateway-description)" : String,
      "[LastUplinkReceivedAt](#cfn-iotwireless-wirelessgateway-lastuplinkreceivedat)" : String,
      "[LoRaWAN](#cfn-iotwireless-wirelessgateway-lorawan)" : LoRaWANGateway,
      "[Name](#cfn-iotwireless-wirelessgateway-name)" : String,
      "[Tags](#cfn-iotwireless-wirelessgateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThingArn](#cfn-iotwireless-wirelessgateway-thingarn)" : String,
      "[ThingName](#cfn-iotwireless-wirelessgateway-thingname)" : String
    }
}
```

### YAML<a name="aws-resource-iotwireless-wirelessgateway-syntax.yaml"></a>

```
Type: AWS::IoTWireless::WirelessGateway
Properties: 
  [Description](#cfn-iotwireless-wirelessgateway-description): String
  [LastUplinkReceivedAt](#cfn-iotwireless-wirelessgateway-lastuplinkreceivedat): String
  [LoRaWAN](#cfn-iotwireless-wirelessgateway-lorawan): 
    LoRaWANGateway
  [Name](#cfn-iotwireless-wirelessgateway-name): String
  [Tags](#cfn-iotwireless-wirelessgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThingArn](#cfn-iotwireless-wirelessgateway-thingarn): String
  [ThingName](#cfn-iotwireless-wirelessgateway-thingname): String
```

## Properties<a name="aws-resource-iotwireless-wirelessgateway-properties"></a>

`Description`  <a name="cfn-iotwireless-wirelessgateway-description"></a>
The description of the new resource\. The maximum length is 2048 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastUplinkReceivedAt`  <a name="cfn-iotwireless-wirelessgateway-lastuplinkreceivedat"></a>
The date and time when the most recent uplink was received\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRaWAN`  <a name="cfn-iotwireless-wirelessgateway-lorawan"></a>
The gateway configuration information to use to create the wireless gateway\.  
*Required*: Yes  
*Type*: [LoRaWANGateway](aws-properties-iotwireless-wirelessgateway-lorawangateway.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-wirelessgateway-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-wirelessgateway-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingArn`  <a name="cfn-iotwireless-wirelessgateway-thingarn"></a>
The ARN of the thing to associate with the wireless gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingName`  <a name="cfn-iotwireless-wirelessgateway-thingname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-wirelessgateway-return-values"></a>

### Ref<a name="aws-resource-iotwireless-wirelessgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the wireless gateway ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-wirelessgateway-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-wirelessgateway-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the wireless gateway created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the wireless gateway created\.