# AWS::EC2::VPNGateway<a name="aws-resource-ec2-vpn-gateway"></a>

Specifies a virtual private gateway\. A virtual private gateway is the endpoint on the VPC side of your VPN connection\. You can create a virtual private gateway before creating the VPC itself\.

For more information, see [AWS Site\-to\-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html) in the *AWS Site\-to\-Site VPN User Guide*\.

## Syntax<a name="aws-resource-ec2-vpn-gateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpn-gateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPNGateway",
  "Properties" : {
      "[AmazonSideAsn](#cfn-ec2-vpngateway-amazonsideasn)" : Long,
      "[Tags](#cfn-ec2-vpngateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-ec2-vpngateway-type)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpn-gateway-syntax.yaml"></a>

```
Type: AWS::EC2::VPNGateway
Properties: 
  [AmazonSideAsn](#cfn-ec2-vpngateway-amazonsideasn): Long
  [Tags](#cfn-ec2-vpngateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-ec2-vpngateway-type): String
```

## Properties<a name="aws-resource-ec2-vpn-gateway-properties"></a>

`AmazonSideAsn`  <a name="cfn-ec2-vpngateway-amazonsideasn"></a>
The private Autonomous System Number \(ASN\) for the Amazon side of a BGP session\.  
*Required*: No  
*Type*: Long  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-vpngateway-tags"></a>
Any tags assigned to the virtual private gateway\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ec2-vpngateway-type"></a>
The type of VPN connection the virtual private gateway supports\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ipsec.1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpn-gateway-return-values"></a>

### Ref<a name="aws-resource-ec2-vpn-gateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPN gateway\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpn-gateway--examples"></a>



### VPN Gateway<a name="aws-resource-ec2-vpn-gateway--examples--VPN_Gateway"></a>

The following example declares a VPN gateway that uses IPSec 1\.

#### JSON<a name="aws-resource-ec2-vpn-gateway--examples--VPN_Gateway--json"></a>

```
"myVPNGateway" : {
   "Type" : "AWS::EC2::VPNGateway",
   "Properties" : {
      "Type" : "ipsec.1",
      "Tags" : [ { "Key" : "Use", "Value" : "Test" } ]
  }
}
```

#### YAML<a name="aws-resource-ec2-vpn-gateway--examples--VPN_Gateway--yaml"></a>

```
  myVPNGateway: 
   Type: AWS::EC2::VPNGateway
   Properties: 
      Type: ipsec.1
      Tags: 
      - Key: Use
        Value: Test
```

## See also<a name="aws-resource-ec2-vpn-gateway--seealso"></a>
+  [CreateVPNGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVPNGateway.html) in the *Amazon EC2 API Reference*

