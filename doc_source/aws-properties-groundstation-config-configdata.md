# AWS::GroundStation::Config ConfigData<a name="aws-properties-groundstation-config-configdata"></a>

 Config objects provide information to Ground Station about how to configure the antenna and how data flows during a contact\. 

## Syntax<a name="aws-properties-groundstation-config-configdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-configdata-syntax.json"></a>

```
{
  "[AntennaDownlinkConfig](#cfn-groundstation-config-configdata-antennadownlinkconfig)" : AntennaDownlinkConfig,
  "[AntennaDownlinkDemodDecodeConfig](#cfn-groundstation-config-configdata-antennadownlinkdemoddecodeconfig)" : AntennaDownlinkDemodDecodeConfig,
  "[AntennaUplinkConfig](#cfn-groundstation-config-configdata-antennauplinkconfig)" : AntennaUplinkConfig,
  "[DataflowEndpointConfig](#cfn-groundstation-config-configdata-dataflowendpointconfig)" : DataflowEndpointConfig,
  "[TrackingConfig](#cfn-groundstation-config-configdata-trackingconfig)" : TrackingConfig,
  "[UplinkEchoConfig](#cfn-groundstation-config-configdata-uplinkechoconfig)" : UplinkEchoConfig
}
```

### YAML<a name="aws-properties-groundstation-config-configdata-syntax.yaml"></a>

```
  [AntennaDownlinkConfig](#cfn-groundstation-config-configdata-antennadownlinkconfig): 
    AntennaDownlinkConfig
  [AntennaDownlinkDemodDecodeConfig](#cfn-groundstation-config-configdata-antennadownlinkdemoddecodeconfig): 
    AntennaDownlinkDemodDecodeConfig
  [AntennaUplinkConfig](#cfn-groundstation-config-configdata-antennauplinkconfig): 
    AntennaUplinkConfig
  [DataflowEndpointConfig](#cfn-groundstation-config-configdata-dataflowendpointconfig): 
    DataflowEndpointConfig
  [TrackingConfig](#cfn-groundstation-config-configdata-trackingconfig): 
    TrackingConfig
  [UplinkEchoConfig](#cfn-groundstation-config-configdata-uplinkechoconfig): 
    UplinkEchoConfig
```

## Properties<a name="aws-properties-groundstation-config-configdata-properties"></a>

`AntennaDownlinkConfig`  <a name="cfn-groundstation-config-configdata-antennadownlinkconfig"></a>
 Provides information for an antenna downlink config object\. Antenna downlink config objects are used to provide parameters for downlinks where no demodulation or decoding is performed by Ground Station \(RF over IP downlinks\)\.   
*Required*: No  
*Type*: [AntennaDownlinkConfig](aws-properties-groundstation-config-antennadownlinkconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AntennaDownlinkDemodDecodeConfig`  <a name="cfn-groundstation-config-configdata-antennadownlinkdemoddecodeconfig"></a>
 Provides information for a downlink demod decode config object\. Downlink demod decode config objects are used to provide parameters for downlinks where the Ground Station service will demodulate and decode the downlinked data\.   
*Required*: No  
*Type*: [AntennaDownlinkDemodDecodeConfig](aws-properties-groundstation-config-antennadownlinkdemoddecodeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AntennaUplinkConfig`  <a name="cfn-groundstation-config-configdata-antennauplinkconfig"></a>
 Provides information for an uplink config object\. Uplink config objects are used to provide parameters for uplink contacts\.   
*Required*: No  
*Type*: [AntennaUplinkConfig](aws-properties-groundstation-config-antennauplinkconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataflowEndpointConfig`  <a name="cfn-groundstation-config-configdata-dataflowendpointconfig"></a>
 Provides information for a dataflow endpoint config object\. Dataflow endpoint config objects are used to provide parameters about which IP endpoint\(s\) to use during a contact\. Dataflow endpoints are where Ground Station sends data during a downlink contact and where Ground Station receives data to send to the satellite during an uplink contact\.   
*Required*: No  
*Type*: [DataflowEndpointConfig](aws-properties-groundstation-config-dataflowendpointconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrackingConfig`  <a name="cfn-groundstation-config-configdata-trackingconfig"></a>
 Provides information for a tracking config object\. Tracking config objects are used to provide parameters about how to track the satellite through the sky during a contact\.   
*Required*: No  
*Type*: [TrackingConfig](aws-properties-groundstation-config-trackingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UplinkEchoConfig`  <a name="cfn-groundstation-config-configdata-uplinkechoconfig"></a>
 Provides information for an uplink echo config object\. Uplink echo config objects are used to provide parameters for uplink echo during uplink contacts\.   
*Required*: No  
*Type*: [UplinkEchoConfig](aws-properties-groundstation-config-uplinkechoconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-configdata--examples"></a>

### Create a ConfigData<a name="aws-properties-groundstation-config-configdata--examples--Create_a_ConfigData"></a>

A `ConfigData` can only contain a single config subtype\. See the config subtype's documentation for more information on its properties\. An example of a `TrackingConfig` is provided below\. 

#### JSON<a name="aws-properties-groundstation-config-configdata--examples--Create_a_ConfigData--json"></a>

```
{
  "TrackingConfig": {
    "Autotrack": "PREFERRED"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-configdata--examples--Create_a_ConfigData--yaml"></a>

```
TrackingConfig:
  Autotrack: "PREFERRED"
```