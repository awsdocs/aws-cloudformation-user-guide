# AWS::NetworkManager::Device<a name="aws-resource-networkmanager-device"></a>

Specifies a device\.

## Syntax<a name="aws-resource-networkmanager-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-device-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::Device",
  "Properties" : {
      "[Description](#cfn-networkmanager-device-description)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-device-globalnetworkid)" : String,
      "[Location](#cfn-networkmanager-device-location)" : Location,
      "[Model](#cfn-networkmanager-device-model)" : String,
      "[SerialNumber](#cfn-networkmanager-device-serialnumber)" : String,
      "[SiteId](#cfn-networkmanager-device-siteid)" : String,
      "[Tags](#cfn-networkmanager-device-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-networkmanager-device-type)" : String,
      "[Vendor](#cfn-networkmanager-device-vendor)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-device-syntax.yaml"></a>

```
Type: AWS::NetworkManager::Device
Properties: 
  [Description](#cfn-networkmanager-device-description): String
  [GlobalNetworkId](#cfn-networkmanager-device-globalnetworkid): String
  [Location](#cfn-networkmanager-device-location): 
    Location
  [Model](#cfn-networkmanager-device-model): String
  [SerialNumber](#cfn-networkmanager-device-serialnumber): String
  [SiteId](#cfn-networkmanager-device-siteid): String
  [Tags](#cfn-networkmanager-device-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-networkmanager-device-type): String
  [Vendor](#cfn-networkmanager-device-vendor): String
```

## Properties<a name="aws-resource-networkmanager-device-properties"></a>

`Description`  <a name="cfn-networkmanager-device-description"></a>
A description of the device\.  
Length Constraints: Maximum length of 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNetworkId`  <a name="cfn-networkmanager-device-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Location`  <a name="cfn-networkmanager-device-location"></a>
The site location\.  
*Required*: No  
*Type*: [Location](aws-properties-networkmanager-device-location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Model`  <a name="cfn-networkmanager-device-model"></a>
The model of the device\.  
Length Constraints: Maximum length of 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SerialNumber`  <a name="cfn-networkmanager-device-serialnumber"></a>
The serial number of the device\.  
Length Constraints: Maximum length of 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SiteId`  <a name="cfn-networkmanager-device-siteid"></a>
The site ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-device-tags"></a>
The tags for the device\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-networkmanager-device-type"></a>
The device type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Vendor`  <a name="cfn-networkmanager-device-vendor"></a>
The vendor of the device\.  
Length Constraints: Maximum length of 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-device-return-values"></a>

### Ref<a name="aws-resource-networkmanager-device-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IDs of the global network and device\. For example: `global-network-01231231231231231|device-07f6fd08867abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-device-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-device-return-values-fn--getatt-fn--getatt"></a>

`DeviceArn`  <a name="DeviceArn-fn::getatt"></a>
The ARN of the device\. For example, `arn:aws:networkmanager::123456789012:device/global-network-01231231231231231/device-07f6fd08867abc123`\.

`DeviceId`  <a name="DeviceId-fn::getatt"></a>
The ID of the device\. For example, `device-07f6fd08867abc123`\.

## Examples<a name="aws-resource-networkmanager-device--examples"></a>



### Device<a name="aws-resource-networkmanager-device--examples--Device"></a>

The following example creates a device in a global network\.

#### JSON<a name="aws-resource-networkmanager-device--examples--Device--json"></a>

```
{
    "Type": "AWS::NetworkManager::Device",
    "Properties": {
        "Description": "Chicago office device",
        "GlobalNetworkId": {
            "Ref": "GlobalNetwork"
        },
        "SiteId": {
            "Fn::GetAtt": [
                "Site",
                "SiteId"
            ]
        },
        "Location": {
            "Address": "227 W Monroe St, Chicago, IL 60606",
            "Latitude": "41.8",
            "Longitude": "-87.6"
        },
        "Tags": [
            {
                "Key": "Network",
                "Value": "north-america"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkmanager-device--examples--Device--yaml"></a>

```
Type: AWS::NetworkManager::Device
Properties:
  Description: "Chicago office device"
  GlobalNetworkId: !Ref GlobalNetwork
  SiteId: !GetAtt Site.SiteId
  Location:
    Address: "227 W Monroe St, Chicago, IL 60606"
    Latitude: "41.8"
    Longitude: "-87.6"
  Tags:
    - Key: Network
      Value: north-america
```