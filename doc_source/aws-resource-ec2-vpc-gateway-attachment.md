# AWS::EC2::VPCGatewayAttachment<a name="aws-resource-ec2-vpc-gateway-attachment"></a>

Attaches a gateway to a VPC\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcgatewayattachment-syntax)
+ [Properties](#w3ab2c21c10d527b9)
+ [Return Values](#w3ab2c21c10d527c11)
+ [Examples](#w3ab2c21c10d527c13)
+ [See Also](#w3ab2c21c10d527c15)

## Syntax<a name="aws-resource-ec2-vpcgatewayattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcgatewayattachment-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPCGatewayAttachment",
   "Properties" : {
      "[InternetGatewayId](#cfn-ec2-vpcgatewayattachment-internetgatewayid)" : String,
      "[VpcId](#cfn-ec2-vpcgatewayattachment-vpcid)" : String,
      "[VpnGatewayId](#cfn-ec2-vpcgatewayattachment-vpngatewayid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpcgatewayattachment-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCGatewayAttachment"
Properties: 
  [InternetGatewayId](#cfn-ec2-vpcgatewayattachment-internetgatewayid): String
  [VpcId](#cfn-ec2-vpcgatewayattachment-vpcid): String
  [VpnGatewayId](#cfn-ec2-vpcgatewayattachment-vpngatewayid): String
```

## Properties<a name="w3ab2c21c10d527b9"></a>

`InternetGatewayId`  <a name="cfn-ec2-vpcgatewayattachment-internetgatewayid"></a>
The ID of the Internet gateway\.  
*Required*: Conditional You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-vpcgatewayattachment-vpcid"></a>
The ID of the VPC to associate with this gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpnGatewayId`  <a name="cfn-ec2-vpcgatewayattachment-vpngatewayid"></a>
The ID of the virtual private network \(VPN\) gateway to attach to the VPC\.  
*Required*: Conditional You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d527c11"></a>

### Ref<a name="w3ab2c21c10d527c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d527c13"></a>

To attach both an Internet gateway and a VPN gateway to a VPC, you must specify two separate `AWS::EC2::VPCGatewayAttachment` resources:

### JSON<a name="aws-resource-ec2-vpcgatewayattachment-example-1.json"></a>

```
"AttachGateway" : {
   "Type" : "AWS::EC2::VPCGatewayAttachment",
   "Properties" : {
      "VpcId" : { "Ref" : "VPC" },
      "InternetGatewayId" : { "Ref" : "myInternetGateway" }
   }
},

"AttachVpnGateway" : {
   "Type" : "AWS::EC2::VPCGatewayAttachment",
   "Properties" : {
      "VpcId" : { "Ref" : "VPC" },
      "VpnGatewayId" : { "Ref" : "myVPNGateway" }
   }
}
```

### YAML<a name="aws-resource-ec2-vpcgatewayattachment-example-1.yaml"></a>

```
AttachGateway:
  Type: AWS::EC2::VPCGatewayAttachment
  Properties:
    VpcId:
      Ref: VPC
    InternetGatewayId:
      Ref: myInternetGateway
AttachVpnGateway:
  Type: AWS::EC2::VPCGatewayAttachment
  Properties:
    VpcId:
      Ref: VPC
    VpnGatewayId:
      Ref: myVPNGateway
```

## See Also<a name="w3ab2c21c10d527c15"></a>
+ [AttachVpnGateway](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AttachVpnGateway.html) in the *Amazon EC2 API Reference*\.