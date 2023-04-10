# AWS::IoTWireless::WirelessDeviceImportTask<a name="aws-resource-iotwireless-wirelessdeviceimporttask"></a>

Information about an import task for wireless devices\. When creating the resource, either create a single wireless device import task using the Sidewalk manufacturing serial number \(SMSN\) of the wireless device, or create an import task for multiple devices by specifying both the `DeviceCreationFile` and the `Role`\.

## Syntax<a name="aws-resource-iotwireless-wirelessdeviceimporttask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-wirelessdeviceimporttask-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::WirelessDeviceImportTask",
  "Properties" : {
      "[DestinationName](#cfn-iotwireless-wirelessdeviceimporttask-destinationname)" : String,
      "[Sidewalk](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk)" : Sidewalk,
      "[Tags](#cfn-iotwireless-wirelessdeviceimporttask-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-wirelessdeviceimporttask-syntax.yaml"></a>

```
Type: AWS::IoTWireless::WirelessDeviceImportTask
Properties: 
  [DestinationName](#cfn-iotwireless-wirelessdeviceimporttask-destinationname): String
  [Sidewalk](#cfn-iotwireless-wirelessdeviceimporttask-sidewalk): 
    Sidewalk
  [Tags](#cfn-iotwireless-wirelessdeviceimporttask-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-wirelessdeviceimporttask-properties"></a>

`DestinationName`  <a name="cfn-iotwireless-wirelessdeviceimporttask-destinationname"></a>
The name of the destination that describes the IoT rule to route messages from the Sidewalk devices in the import task to other applications\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sidewalk`  <a name="cfn-iotwireless-wirelessdeviceimporttask-sidewalk"></a>
The Sidewalk\-related information of the wireless device import task\.  
*Required*: Yes  
*Type*: [Sidewalk](aws-properties-iotwireless-wirelessdeviceimporttask-sidewalk.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-wirelessdeviceimporttask-tags"></a>
Adds to or modifies the tags of the given resource\. Tags are metadata that you can use to manage a resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-wirelessdeviceimporttask-return-values"></a>

### Ref<a name="aws-resource-iotwireless-wirelessdeviceimporttask-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the wireless device import task\.

### Fn::GetAtt<a name="aws-resource-iotwireless-wirelessdeviceimporttask-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-wirelessdeviceimporttask-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN \(Amazon Resource Name\) of the import task\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The date and time at which the wireless device import task was created\.

`FailedImportedDevicesCount`  <a name="FailedImportedDevicesCount-fn::getatt"></a>
The summary information of count of wireless devices that failed to onboard to the import task\.

`Id`  <a name="Id-fn::getatt"></a>
The import task ID\.

`InitializedImportedDevicesCount`  <a name="InitializedImportedDevicesCount-fn::getatt"></a>
The summary information of count of wireless devices that are waiting for the control log to be added to an import task\.

`OnboardedImportedDevicesCount`  <a name="OnboardedImportedDevicesCount-fn::getatt"></a>
The summary information of count of wireless devices that have been onboarded to the import task\.

`PendingImportedDevicesCount`  <a name="PendingImportedDevicesCount-fn::getatt"></a>
The summary information of count of wireless devices that are waiting in the queue to be onboarded to the import task\.

`Status`  <a name="Status-fn::getatt"></a>
The status of a wireless device import task\. The status can be `INITIALIZING`, `INITIALIZED`, `PENDING`, `COMPLETE`, `FAILED`, or `DELETING`\.

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
The reason that provides additional information about the import task status\.