# AWS::IoTFleetWise::DecoderManifest NetworkInterfacesItems<a name="aws-properties-iotfleetwise-decodermanifest-networkinterfacesitems"></a>

\(Optional\) A list of information about available network interfaces\. 

## Syntax<a name="aws-properties-iotfleetwise-decodermanifest-networkinterfacesitems-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-decodermanifest-networkinterfacesitems-syntax.json"></a>

```
{
  "[CanInterface](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-caninterface)" : CanInterface,
  "[InterfaceId](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-interfaceid)" : String,
  "[ObdInterface](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-obdinterface)" : ObdInterface,
  "[Type](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-type)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-decodermanifest-networkinterfacesitems-syntax.yaml"></a>

```
  [CanInterface](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-caninterface): 
    CanInterface
  [InterfaceId](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-interfaceid): String
  [ObdInterface](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-obdinterface): 
    ObdInterface
  [Type](#cfn-iotfleetwise-decodermanifest-networkinterfacesitems-type): String
```

## Properties<a name="aws-properties-iotfleetwise-decodermanifest-networkinterfacesitems-properties"></a>

`CanInterface`  <a name="cfn-iotfleetwise-decodermanifest-networkinterfacesitems-caninterface"></a>
\(Optional\) Information about a network interface specified by the Controller Area Network \(CAN\) protocol\.  
*Required*: No  
*Type*: [CanInterface](aws-properties-iotfleetwise-decodermanifest-caninterface.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InterfaceId`  <a name="cfn-iotfleetwise-decodermanifest-networkinterfacesitems-interfaceid"></a>
The ID of the network interface\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObdInterface`  <a name="cfn-iotfleetwise-decodermanifest-networkinterfacesitems-obdinterface"></a>
\(Optional\) Information about a network interface specified by the On\-board diagnostic \(OBD\) II protocol\.  
*Required*: No  
*Type*: [ObdInterface](aws-properties-iotfleetwise-decodermanifest-obdinterface.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotfleetwise-decodermanifest-networkinterfacesitems-type"></a>
The network protocol for the vehicle\. For example, `CAN_SIGNAL` specifies a protocol that defines how data is communicated between electronic control units \(ECUs\)\. `OBD_SIGNAL` specifies a protocol that defines how self\-diagnostic data is communicated between ECUs\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CAN_INTERFACE | OBD_INTERFACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)