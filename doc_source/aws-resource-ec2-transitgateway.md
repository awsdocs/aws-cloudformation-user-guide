# AWS::EC2::TransitGateway<a name="aws-resource-ec2-transitgateway"></a>

Creates a transit gateway\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgateway-syntax)
+ [Properties](#aws-resource-ec2-transitgateway-properties)
+ [Return Values](#aws-resource-ec2-transitgateway-returnvalues)
+ [Example](#aws-resource-ec2-transitgateway-examples)
+ [See Also](#aws-resource-ec2-transitgateway-seealso)

## Syntax<a name="aws-resource-ec2-transitgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGateway",
  "Properties" : {
    "[AmazonSideAsn](#cfn-ec2-transitgateway-amazonsideasn)" : Integer,
    "[AutoAcceptSharedAttachments](#cfn-ec2-transitgateway-autoacceptsharedattachments)" : String,
    "[DefaultRouteTableAssociation](#cfn-ec2-transitgateway-defaultroutetableassociation)" : String,
    "[DefaultRouteTablePropagation](#cfn-ec2-transitgateway-defaultroutetablepropagation)" : String,
    "[Description](#cfn-ec2-transitgateway-description)" : String,
    "[DnsSupport](#cfn-ec2-transitgateway-dnssupport)" : String,
    "[Tags](#cfn-ec2-transitgateway-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[VpnEcmpSupport](#cfn-ec2-transitgateway-vpnecmpsupport)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgateway-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGateway"
Properties:
  [AmazonSideAsn](#cfn-ec2-transitgateway-amazonsideasn): Integer
  [AutoAcceptSharedAttachments](#cfn-ec2-transitgateway-autoacceptsharedattachments): String
  [DefaultRouteTableAssociation](#cfn-ec2-transitgateway-defaultroutetableassociation): String
  [DefaultRouteTablePropagation](#cfn-ec2-transitgateway-defaultroutetablepropagation): String
  [Description](#cfn-ec2-transitgateway-description): String
  [DnsSupport](#cfn-ec2-transitgateway-dnssupport): String
  [Tags](#cfn-ec2-transitgateway-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [VpnEcmpSupport](#cfn-ec2-transitgateway-vpnecmpsupport): String
```

## Properties<a name="aws-resource-ec2-transitgateway-properties"></a>

`AmazonSideAsn`  <a name="cfn-ec2-transitgateway-amazonsideasn"></a>
A private Autonomous System Number \(ASN\) for the Amazon side of a BGP session\. The range is 64512 to 65534 for 16\-bit ASNs and 4200000000 to 4294967294 for 32\-bit ASNs\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AutoAcceptSharedAttachments`  <a name="cfn-ec2-transitgateway-autoacceptsharedattachments"></a>
Indicates whether attachment requests are automatically accepted\. The default is `disable`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DefaultRouteTableAssociation`  <a name="cfn-ec2-transitgateway-defaultroutetableassociation"></a>
Enable or disable automatic association with the default association route table\. The default is `enable`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DefaultRouteTablePropagation`  <a name="cfn-ec2-transitgateway-defaultroutetablepropagation"></a>
Enable or disable automatic propagation of routes to the default propagation route table\. The default is `enable`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Description`  <a name="cfn-ec2-transitgateway-description"></a>
A description of the transit gateway\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DnsSupport`  <a name="cfn-ec2-transitgateway-dnssupport"></a>
Enable or disable DNS support\. The default is `enable`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-ec2-transitgateway-tags"></a>
The tags to apply to the transit gateway\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VpnEcmpSupport`  <a name="cfn-ec2-transitgateway-vpnecmpsupport"></a>
Enable or disable Equal Cost Multipath Protocol\. The default is `enable`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgateway-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgateway-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGateway` resource to the intrinsic `Ref` function, the function returns the ID of the transit gateway, such as `tgw-1234567891234567`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-ec2-transitgateway-examples"></a>

### JSON<a name="aws-resource-ec2-transitgateway-example1.json"></a>

```
{
    "Resources": {
        "myTransitGateway": {
            "Type": "AWS::EC2::TransitGateway",
            "Properties": {
                "AmazonSideAsn": 65000,
                "Description": "TGW Route Integration Test",
                "AutoAcceptSharedAttachments": "disable",
                "DefaultRouteTableAssociation": "enable",
                "DnsSupport": "enable",
                "VpnEcmpSupport": "enable",
                "Tags": [
                    {
                        "Key": "Application",
                        "Value": {
                            "Ref": "AWS::StackId"
                        }
                    }
                ]
            }
        }
    }
}
```

### YAML<a name="aws-resource-ec2-transitgateway-example1.yaml"></a>

```
Resources:
  myTransitGateway:
    Type: "AWS::EC2::TransitGateway"
    Properties:
      AmazonSideAsn: 65000
      Description: "TGW Route Integration Test"
      AutoAcceptSharedAttachments: "disable"
      DefaultRouteTableAssociation: "enable"
      DnsSupport: "enable"
      VpnEcmpSupport: "enable"
      Tags:
      - Key: Application
        Value: !Ref 'AWS::StackId'
```

## See Also<a name="aws-resource-ec2-transitgateway-seealso"></a>
+ [CreateTransitGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGateway.html) in the *Amazon EC2 API Reference*
+ [ModifyTransitGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyTransitGateway.html) in the *Amazon EC2 API Reference*
