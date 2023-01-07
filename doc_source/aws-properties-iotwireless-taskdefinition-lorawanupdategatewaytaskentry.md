# AWS::IoTWireless::TaskDefinition LoRaWANUpdateGatewayTaskEntry<a name="aws-properties-iotwireless-taskdefinition-lorawanupdategatewaytaskentry"></a>

LoRaWANUpdateGatewayTaskEntry object\.

## Syntax<a name="aws-properties-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-syntax.json"></a>

```
{
  "[CurrentVersion](#cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-currentversion)" : LoRaWANGatewayVersion,
  "[UpdateVersion](#cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-updateversion)" : LoRaWANGatewayVersion
}
```

### YAML<a name="aws-properties-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-syntax.yaml"></a>

```
  [CurrentVersion](#cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-currentversion): 
    LoRaWANGatewayVersion
  [UpdateVersion](#cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-updateversion): 
    LoRaWANGatewayVersion
```

## Properties<a name="aws-properties-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-properties"></a>

`CurrentVersion`  <a name="cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-currentversion"></a>
The version of the gateways that should receive the update\.  
*Required*: No  
*Type*: [LoRaWANGatewayVersion](aws-properties-iotwireless-taskdefinition-lorawangatewayversion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateVersion`  <a name="cfn-iotwireless-taskdefinition-lorawanupdategatewaytaskentry-updateversion"></a>
The firmware version to update the gateway to\.  
*Required*: No  
*Type*: [LoRaWANGatewayVersion](aws-properties-iotwireless-taskdefinition-lorawangatewayversion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)