# AWS::NetworkManager::LinkAssociation<a name="aws-resource-networkmanager-linkassociation"></a>

Specifies the association between a device and a link\. A device can be associated to multiple links and a link can be associated to multiple devices\. The device and link must be in the same global network and the same site\.

## Syntax<a name="aws-resource-networkmanager-linkassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-linkassociation-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::LinkAssociation",
  "Properties" : {
      "[DeviceId](#cfn-networkmanager-linkassociation-deviceid)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-linkassociation-globalnetworkid)" : String,
      "[LinkId](#cfn-networkmanager-linkassociation-linkid)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-linkassociation-syntax.yaml"></a>

```
Type: AWS::NetworkManager::LinkAssociation
Properties: 
  [DeviceId](#cfn-networkmanager-linkassociation-deviceid): String
  [GlobalNetworkId](#cfn-networkmanager-linkassociation-globalnetworkid): String
  [LinkId](#cfn-networkmanager-linkassociation-linkid): String
```

## Properties<a name="aws-resource-networkmanager-linkassociation-properties"></a>

`DeviceId`  <a name="cfn-networkmanager-linkassociation-deviceid"></a>
The device ID for the link association\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GlobalNetworkId`  <a name="cfn-networkmanager-linkassociation-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LinkId`  <a name="cfn-networkmanager-linkassociation-linkid"></a>
The ID of the link\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-linkassociation-return-values"></a>

### Ref<a name="aws-resource-networkmanager-linkassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IDs of the global network, device, and link\. For example: `global-network-01231231231231231|device-07f6fd08867abc123|link-11112222aaaabbbb1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-networkmanager-linkassociation--examples"></a>



### Link Association<a name="aws-resource-networkmanager-linkassociation--examples--Link_Association"></a>

The following example template creates a global network, site, link, and device\. It creates an association between the link and the device\.

#### JSON<a name="aws-resource-networkmanager-linkassociation--examples--Link_Association--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Create global network and link association",
    "Resources": {
        "GlobalNetwork": {
            "Type": "AWS::NetworkManager::GlobalNetwork"
        },
        "Site": {
            "Type": "AWS::NetworkManager::Site",
            "Properties": {
                "GlobalNetworkId": {
                    "Ref": "GlobalNetwork"
                },
                "Location": {
                    "Address": "227 W Monroe St, Chicago, IL 60606",
                    "Latitude": "41.8",
                    "Longitude": "-87.6"
                }
            }
        },
        "Link": {
            "Type": "AWS::NetworkManager::Link",
            "Properties": {
                "Description": "Broadband link",
                "GlobalNetworkId": {
                    "Ref": "GlobalNetwork"
                },
                "SiteId": {
                    "Fn::GetAtt": [
                        "Site",
                        "SiteId"
                    ]
                },
                "Bandwidth": {
                    "DownloadSpeed": 20,
                    "UploadSpeed": 20
                },
                "Provider": "AnyCompany",
                "Type": "Broadband",
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "broadband-link-1"
                    }
                ]
            }
        },
        "Device": {
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
                "Tags": [
                    {
                        "Key": "Network",
                        "Value": "north-america"
                    }
                ]
            }
        },
        "LinkAssociation": {
            "Type": "AWS::NetworkManager::LinkAssociation",
            "Properties": {
                "GlobalNetworkId": {
                    "Ref": "GlobalNetwork"
                },
                "LinkId": {
                    "Fn::GetAtt": [
                        "Link",
                        "LinkId"
                    ]
                },
                "DeviceId": {
                    "Fn::GetAtt": [
                        "Device",
                        "DeviceId"
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-networkmanager-linkassociation--examples--Link_Association--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'Create global network and link association'
Resources:
  GlobalNetwork:
    Type: AWS::NetworkManager::GlobalNetwork
  Site:
    Type: AWS::NetworkManager::Site
    Properties:
      GlobalNetworkId: !Ref GlobalNetwork
      Location:
        Address: "227 W Monroe St, Chicago, IL 60606"
        Latitude: "41.8"
        Longitude: "-87.6"
  Link:
    Type: AWS::NetworkManager::Link
    Properties:
      Description: Broadband link
      GlobalNetworkId: !Ref GlobalNetwork
      SiteId: !GetAtt Site.SiteId
      Bandwidth:
        DownloadSpeed: 20
        UploadSpeed: 20
      Provider: "AnyCompany"
      Type: "Broadband"
      Tags:
        - Key: Name
          Value: broadband-link-1
  Device:
    Type: AWS::NetworkManager::Device
    Properties:
      Description: Chicago office device
      GlobalNetworkId: !Ref GlobalNetwork
      SiteId: !GetAtt Site.SiteId
      Tags:
        - Key: Network
          Value: north-america
  LinkAssociation:
    Type: AWS::NetworkManager::LinkAssociation
    Properties:
      GlobalNetworkId: !Ref GlobalNetwork
      LinkId: !GetAtt Link.LinkId
      DeviceId: !GetAtt Device.DeviceId
```