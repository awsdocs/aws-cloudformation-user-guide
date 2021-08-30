# AWS::NetworkManager::CustomerGatewayAssociation<a name="aws-resource-networkmanager-customergatewayassociation"></a>

Specifies an association between a customer gateway, a device, and optionally, a link\. If you specify a link, it must be associated with the specified device\. The customer gateway must be connected to a VPN attachment on a transit gateway that's registered in your global network\.

You cannot associate a customer gateway with more than one device and link\.

## Syntax<a name="aws-resource-networkmanager-customergatewayassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-customergatewayassociation-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::CustomerGatewayAssociation",
  "Properties" : {
      "[CustomerGatewayArn](#cfn-networkmanager-customergatewayassociation-customergatewayarn)" : String,
      "[DeviceId](#cfn-networkmanager-customergatewayassociation-deviceid)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-customergatewayassociation-globalnetworkid)" : String,
      "[LinkId](#cfn-networkmanager-customergatewayassociation-linkid)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-customergatewayassociation-syntax.yaml"></a>

```
Type: AWS::NetworkManager::CustomerGatewayAssociation
Properties: 
  [CustomerGatewayArn](#cfn-networkmanager-customergatewayassociation-customergatewayarn): String
  [DeviceId](#cfn-networkmanager-customergatewayassociation-deviceid): String
  [GlobalNetworkId](#cfn-networkmanager-customergatewayassociation-globalnetworkid): String
  [LinkId](#cfn-networkmanager-customergatewayassociation-linkid): String
```

## Properties<a name="aws-resource-networkmanager-customergatewayassociation-properties"></a>

`CustomerGatewayArn`  <a name="cfn-networkmanager-customergatewayassociation-customergatewayarn"></a>
The Amazon Resource Name \(ARN\) of the customer gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeviceId`  <a name="cfn-networkmanager-customergatewayassociation-deviceid"></a>
The ID of the device\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GlobalNetworkId`  <a name="cfn-networkmanager-customergatewayassociation-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LinkId`  <a name="cfn-networkmanager-customergatewayassociation-linkid"></a>
The ID of the link\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-customergatewayassociation-return-values"></a>

### Ref<a name="aws-resource-networkmanager-customergatewayassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the global network and the Amazon Resource Name \(ARN\) of the customer gateway\. For example: `global-network-01231231231231231|arn:aws:ec2:eu-central-1:123456789012:customer-gateway/cgw-00112233aabbcc112`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-networkmanager-customergatewayassociation--examples"></a>



### Customer Gateway Association<a name="aws-resource-networkmanager-customergatewayassociation--examples--Customer_Gateway_Association"></a>

The following example template creates a global network, device, customer gateway, VPN connection, and transit gateway\. It registers the transit gateway in the global network, and creates an association between the customer gateway and device\. The creation of the customer gateway association depends on the VPN connection and transit gateway registration\.

#### JSON<a name="aws-resource-networkmanager-customergatewayassociation--examples--Customer_Gateway_Association--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Create a global network and customer gateway association",
    "Resources": {
        "GlobalNetwork": {
            "Type": "AWS::NetworkManager::GlobalNetwork"
        },
        "Device": {
            "Type": "AWS::NetworkManager::Device",
            "Properties": {
                "Description": "Chicago office device",
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
        "TransitGateway": {
            "Type": "AWS::EC2::TransitGateway"
        },
        "TransitGatewayRegistration": {
            "Type": "AWS::NetworkManager::TransitGatewayRegistration",
            "Properties": {
                "GlobalNetworkId": {
                    "Ref": "GlobalNetwork"
                },
                "TransitGatewayArn": {
                    "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:transit-gateway/${TransitGateway}"
                }
            }
        },
        "CustomerGateway": {
            "Type": "AWS::EC2::CustomerGateway",
            "Properties": {
                "Type": "ipsec.1",
                "BgpAsn": 65534,
                "IpAddress": "12.1.2.3"
            }
        },
        "VPNConnection": {
            "Type": "AWS::EC2::VPNConnection",
            "Properties": {
                "Type": "ipsec.1",
                "StaticRoutesOnly": true,
                "CustomerGatewayId": {
                    "Ref": "CustomerGateway"
                },
                "TransitGatewayId": {
                    "Ref": "TransitGateway"
                }
            }
        },
        "CustomerGatewayAssociation": {
            "DependsOn": [
                "VPNConnection",
                "TransitGatewayRegistration"
            ],
            "Type": "AWS::NetworkManager::CustomerGatewayAssociation",
            "Properties": {
                "GlobalNetworkId": {
                    "Ref": "GlobalNetwork"
                },
                "DeviceId": {
                    "Fn::GetAtt": [
                        "Device",
                        "DeviceId"
                    ]
                },
                "CustomerGatewayArn": {
                    "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:customer-gateway/${CustomerGateway}"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-networkmanager-customergatewayassociation--examples--Customer_Gateway_Association--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'Create a global network and customer gateway association'
Resources:
  GlobalNetwork:
    Type: AWS::NetworkManager::GlobalNetwork
  Device:
    Type: AWS::NetworkManager::Device
    Properties:
      Description: Chicago office device
      GlobalNetworkId: !Ref GlobalNetwork
      Location:
        Address: "227 W Monroe St, Chicago, IL 60606"
        Latitude: "41.8"
        Longitude: "-87.6"
  TransitGateway:
    Type: AWS::EC2::TransitGateway
  TransitGatewayRegistration:
    Type: AWS::NetworkManager::TransitGatewayRegistration
    Properties:
      GlobalNetworkId: !Ref GlobalNetwork
      TransitGatewayArn: !Sub 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:transit-gateway/${TransitGateway}'
  CustomerGateway:
    Type: AWS::EC2::CustomerGateway
    Properties:
      Type: ipsec.1
      BgpAsn: 65534
      IpAddress: 12.1.2.3
  VPNConnection:
    Type: AWS::EC2::VPNConnection
    Properties:
      Type: ipsec.1
      StaticRoutesOnly: true
      CustomerGatewayId:
        !Ref CustomerGateway
      TransitGatewayId:
        !Ref TransitGateway
  CustomerGatewayAssociation:
    DependsOn:
      - VPNConnection
      - TransitGatewayRegistration
    Type: AWS::NetworkManager::CustomerGatewayAssociation
    Properties:
      GlobalNetworkId: !Ref GlobalNetwork
      DeviceId: !GetAtt Device.DeviceId
      CustomerGatewayArn: !Sub 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:customer-gateway/${CustomerGateway}'
```