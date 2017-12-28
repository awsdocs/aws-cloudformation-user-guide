# AWS::EC2::VPCGatewayAttachment<a name="aws-resource-ec2-vpc-gateway-attachment"></a>

Attaches a gateway to a VPC\.


+ [Syntax](#aws-resource-ec2-vpcgatewayattachment-syntax)
+ [Properties](#w3ab2c21c10d486b9)
+ [Return Values](#w3ab2c21c10d486c11)
+ [Examples](#w3ab2c21c10d486c13)
+ [See Also](#w3ab2c21c10d486c15)

## Syntax<a name="aws-resource-ec2-vpcgatewayattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcgatewayattachment-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPCGatewayAttachment",
   "Properties" : {
      "InternetGatewayId" : String,
      "VpcId" : String,
      "VpnGatewayId" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpcgatewayattachment-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCGatewayAttachment"
Properties: 
  InternetGatewayId: String
  VpcId: String
  VpnGatewayId: String
```

## Properties<a name="w3ab2c21c10d486b9"></a>

`InternetGatewayId`  
The ID of the Internet gateway\.  
*Required: *Conditional You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Type*: String  
*Update requires*: No interruption

`VpcId`  
The ID of the VPC to associate with this gateway\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`VpnGatewayId`  
The ID of the virtual private network \(VPN\) gateway to attach to the VPC\.  
*Required: *Conditional You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Type*: String  
*Update requires*: No interruption

## Return Values<a name="w3ab2c21c10d486c11"></a>

### Ref<a name="w3ab2c21c10d486c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Examples<a name="w3ab2c21c10d486c13"></a>

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

## See Also<a name="w3ab2c21c10d486c15"></a>

+ [AttachVpnGateway](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AttachVpnGateway.html) in the *Amazon EC2 API Reference*\.