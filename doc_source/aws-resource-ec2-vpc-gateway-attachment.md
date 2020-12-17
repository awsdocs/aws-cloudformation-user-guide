# AWS::EC2::VPCGatewayAttachment<a name="aws-resource-ec2-vpc-gateway-attachment"></a>

Attaches an internet gateway, or a virtual private gateway to a VPC, enabling connectivity between the internet and the VPC\.

## Syntax<a name="aws-resource-ec2-vpc-gateway-attachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpc-gateway-attachment-syntax.json"></a>

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

### YAML<a name="aws-resource-ec2-vpc-gateway-attachment-syntax.yaml"></a>

```
Type: AWS::EC2::VPCGatewayAttachment
Properties: 
  [InternetGatewayId](#cfn-ec2-vpcgatewayattachment-internetgatewayid): String
  [VpcId](#cfn-ec2-vpcgatewayattachment-vpcid): String
  [VpnGatewayId](#cfn-ec2-vpcgatewayattachment-vpngatewayid): String
```

## Properties<a name="aws-resource-ec2-vpc-gateway-attachment-properties"></a>

`InternetGatewayId`  <a name="cfn-ec2-vpcgatewayattachment-internetgatewayid"></a>
The ID of the internet gateway\.  
You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-vpcgatewayattachment-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpnGatewayId`  <a name="cfn-ec2-vpcgatewayattachment-vpngatewayid"></a>
The ID of the virtual private gateway\.  
You must specify either `InternetGatewayId` or `VpnGatewayId`, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-vpc-gateway-attachment-return-values"></a>

### Ref<a name="aws-resource-ec2-vpc-gateway-attachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC gateway attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpc-gateway-attachment--examples"></a>



### VPN Gateway Attachment<a name="aws-resource-ec2-vpc-gateway-attachment--examples--VPN_Gateway_Attachment"></a>

To attach both an Internet gateway and a VPN gateway to a VPC, you must specify two separate AWS::EC2::VPCGatewayAttachment resources: 

#### JSON<a name="aws-resource-ec2-vpc-gateway-attachment--examples--VPN_Gateway_Attachment--json"></a>

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

#### YAML<a name="aws-resource-ec2-vpc-gateway-attachment--examples--VPN_Gateway_Attachment--yaml"></a>

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

## See also<a name="aws-resource-ec2-vpc-gateway-attachment--seealso"></a>
+  [AttachVpnGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AttachVpnGateway.html) in the *Amazon EC2 API Reference*
+ [InternetGateways](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html) in the *Amazon Virtual Private Cloud User Guide*

