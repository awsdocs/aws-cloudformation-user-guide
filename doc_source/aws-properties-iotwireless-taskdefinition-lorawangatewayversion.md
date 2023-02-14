# AWS::IoTWireless::TaskDefinition LoRaWANGatewayVersion<a name="aws-properties-iotwireless-taskdefinition-lorawangatewayversion"></a>

LoRaWANGatewayVersion object\.

## Syntax<a name="aws-properties-iotwireless-taskdefinition-lorawangatewayversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-taskdefinition-lorawangatewayversion-syntax.json"></a>

```
{
  "[Model](#cfn-iotwireless-taskdefinition-lorawangatewayversion-model)" : String,
  "[PackageVersion](#cfn-iotwireless-taskdefinition-lorawangatewayversion-packageversion)" : String,
  "[Station](#cfn-iotwireless-taskdefinition-lorawangatewayversion-station)" : String
}
```

### YAML<a name="aws-properties-iotwireless-taskdefinition-lorawangatewayversion-syntax.yaml"></a>

```
  [Model](#cfn-iotwireless-taskdefinition-lorawangatewayversion-model): String
  [PackageVersion](#cfn-iotwireless-taskdefinition-lorawangatewayversion-packageversion): String
  [Station](#cfn-iotwireless-taskdefinition-lorawangatewayversion-station): String
```

## Properties<a name="aws-properties-iotwireless-taskdefinition-lorawangatewayversion-properties"></a>

`Model`  <a name="cfn-iotwireless-taskdefinition-lorawangatewayversion-model"></a>
The model number of the wireless gateway\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PackageVersion`  <a name="cfn-iotwireless-taskdefinition-lorawangatewayversion-packageversion"></a>
The version of the wireless gateway firmware\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Station`  <a name="cfn-iotwireless-taskdefinition-lorawangatewayversion-station"></a>
The basic station version of the wireless gateway\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)