# AWS::EC2::VPNGateway<a name="aws-resource-ec2-vpn-gateway"></a>

Creates a virtual private gateway\. A virtual private gateway is the VPC\-side endpoint for your VPN connection\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcgateway-syntax)
+ [Properties](#w3ab2c21c10d546b9)
+ [Return Value](#w3ab2c21c10d546c11)
+ [Example](#w3ab2c21c10d546c13)
+ [See Also](#w3ab2c21c10d546c15)

## Syntax<a name="aws-resource-ec2-vpcgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcgateway-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPNGateway",
   "Properties" : {
      "[AmazonSideAsn](#cfn-ec2-vpngateway-amazonsideasn)" : Long,
      "[Type](#cfn-ec2-vpngateway-type)" : String,
      "[Tags](#cfn-ec2-vpngateway-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-vpcgateway-syntax.yaml"></a>

```
Type: "AWS::EC2::VPNGateway"
Properties: 
  [AmazonSideAsn](#cfn-ec2-vpngateway-amazonsideasn): Long
  [Type](#cfn-ec2-vpngateway-type): String
  [Tags](#cfn-ec2-vpngateway-tags):
    Resource Tag
```

## Properties<a name="w3ab2c21c10d546b9"></a>

`AmazonSideAsn`  <a name="cfn-ec2-vpngateway-amazonsideasn"></a>
The private Autonomous System Number \(ASN\) for the Amazon side of a BGP session\.  
*Required*: No  
*Type*: Long  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Type`  <a name="cfn-ec2-vpngateway-type"></a>
The type of VPN connection this virtual private gateway supports\. The only valid value is `"ipsec.1"`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-vpngateway-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this resource\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

## Return Value<a name="w3ab2c21c10d546c11"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyVPNGateway" }
```

For the VPN gateway with the logical ID "MyVPNGateway", `Ref` will return the gateway's resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d546c13"></a>

### JSON<a name="aws-resource-ec2-vpcgateway-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myVPNGateway" : {
         "Type" : "AWS::EC2::VPNGateway",
         "Properties" : {
            "Type" : "ipsec.1",
            "Tags" : [ { "Key" : "Use", "Value" : "Test" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-vpcgateway-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myVPNGateway: 
    Type: "AWS::EC2::VPNGateway"
    Properties: 
      Type: ipsec.1
      Tags: 
        - 
          Key: Use
          Value: Test
```

## See Also<a name="w3ab2c21c10d546c15"></a>
+ [CreateVpnGateway](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpnGateway.html) in the *Amazon EC2 API Reference*\.