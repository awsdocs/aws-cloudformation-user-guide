# AWS::IoTWireless::DeviceProfile LoRaWANDeviceProfile<a name="aws-properties-iotwireless-deviceprofile-lorawandeviceprofile"></a>

LoRaWANDeviceProfile object\.

## Syntax<a name="aws-properties-iotwireless-deviceprofile-lorawandeviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-deviceprofile-lorawandeviceprofile-syntax.json"></a>

```
{
  "[ClassBTimeout](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-classbtimeout)" : Integer,
  "[ClassCTimeout](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-classctimeout)" : Integer,
  "[MacVersion](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-macversion)" : String,
  "[MaxDutyCycle](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxdutycycle)" : Integer,
  "[MaxEirp](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxeirp)" : Integer,
  "[PingSlotDr](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotdr)" : Integer,
  "[PingSlotFreq](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotfreq)" : Integer,
  "[PingSlotPeriod](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotperiod)" : Integer,
  "[RegParamsRevision](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-regparamsrevision)" : String,
  "[RfRegion](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-rfregion)" : String,
  "[Supports32BitFCnt](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supports32bitfcnt)" : Boolean,
  "[SupportsClassB](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassb)" : Boolean,
  "[SupportsClassC](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassc)" : Boolean,
  "[SupportsJoin](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsjoin)" : Boolean
}
```

### YAML<a name="aws-properties-iotwireless-deviceprofile-lorawandeviceprofile-syntax.yaml"></a>

```
  [ClassBTimeout](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-classbtimeout): Integer
  [ClassCTimeout](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-classctimeout): Integer
  [MacVersion](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-macversion): String
  [MaxDutyCycle](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxdutycycle): Integer
  [MaxEirp](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxeirp): Integer
  [PingSlotDr](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotdr): Integer
  [PingSlotFreq](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotfreq): Integer
  [PingSlotPeriod](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotperiod): Integer
  [RegParamsRevision](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-regparamsrevision): String
  [RfRegion](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-rfregion): String
  [Supports32BitFCnt](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supports32bitfcnt): Boolean
  [SupportsClassB](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassb): Boolean
  [SupportsClassC](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassc): Boolean
  [SupportsJoin](#cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsjoin): Boolean
```

## Properties<a name="aws-properties-iotwireless-deviceprofile-lorawandeviceprofile-properties"></a>

`ClassBTimeout`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-classbtimeout"></a>
The ClassBTimeout value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClassCTimeout`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-classctimeout"></a>
The ClassCTimeout value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MacVersion`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-macversion"></a>
The MAC version \(such as OTAA 1\.1 or OTAA 1\.0\.3\) to use with this device profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxDutyCycle`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxdutycycle"></a>
The MaxDutyCycle value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxEirp`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-maxeirp"></a>
The MaxEIRP value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PingSlotDr`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotdr"></a>
The PingSlotDR value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PingSlotFreq`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotfreq"></a>
The PingSlotFreq value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PingSlotPeriod`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-pingslotperiod"></a>
The PingSlotPeriod value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegParamsRevision`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-regparamsrevision"></a>
The version of regional parameters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RfRegion`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-rfregion"></a>
The frequency band \(RFRegion\) value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Supports32BitFCnt`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-supports32bitfcnt"></a>
The Supports32BitFCnt value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportsClassB`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassb"></a>
The SupportsClassB value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportsClassC`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsclassc"></a>
The SupportsClassC value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportsJoin`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile-supportsjoin"></a>
The SupportsJoin value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)