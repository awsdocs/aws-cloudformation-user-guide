# AWS::IoTWireless::WirelessDeviceImportTask Sidewalk<a name="aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk"></a>

Sidewalk\-related information about a wireless device import task\.

## Syntax<a name="aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk-syntax.json"></a>

```
{
  "[DeviceCreationFile](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfile)" : String,
  "[DeviceCreationFileList](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfilelist)" : [ String, ... ],
  "[Role](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-role)" : String,
  "[SidewalkManufacturingSn](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-sidewalkmanufacturingsn)" : String
}
```

### YAML<a name="aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk-syntax.yaml"></a>

```
  [DeviceCreationFile](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfile): String
  [DeviceCreationFileList](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfilelist): 
    - String
  [Role](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-role): String
  [SidewalkManufacturingSn](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk-sidewalkmanufacturingsn): String
```

## Properties<a name="aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk-properties"></a>

`DeviceCreationFile`  <a name="cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfile"></a>
The CSV file contained in an S3 bucket that's used for adding devices to an import task\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceCreationFileList`  <a name="cfn-iotwireless-wirelessdeviceimporttask-sidewalk-devicecreationfilelist"></a>
List of Sidewalk devices that are added to the import task\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-iotwireless-wirelessdeviceimporttask-sidewalk-role"></a>
The IAM role that allows AWS IoT Wireless to access the CSV file in the S3 bucket\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SidewalkManufacturingSn`  <a name="cfn-iotwireless-wirelessdeviceimporttask-sidewalk-sidewalkmanufacturingsn"></a>
The Sidewalk manufacturing serial number \(SMSN\) of the Sidewalk device\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)