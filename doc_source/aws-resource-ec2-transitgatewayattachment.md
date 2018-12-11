# AWS::EC2::TransitGatewayAttachment<a name="aws-resource-ec2-transitgatewayattachment"></a>

Creates an attachment between a VPC and a transit gateway\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgatewayattachment-syntax)
+ [Properties](#aws-resource-ec2-transitgatewayattachment-properties)
+ [Return Values](#aws-resource-ec2-transitgatewayattachment-returnvalues)
+ [See Also](#aws-resource-ec2-transitgatewayattachment-seealso)

## Syntax<a name="aws-resource-ec2-transitgatewayattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayAttachment",
  "Properties" : {
    "[SubnetIds](#cfn-ec2-transitgatewayattachment-subnetids)" : [ String, ... ],
    "[Tags](#cfn-ec2-transitgatewayattachment-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[TransitGatewayId](#cfn-ec2-transitgatewayattachment-transitgatewayid)" : String,
    "[VpcId](#cfn-ec2-transitgatewayattachment-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayattachment-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGatewayAttachment"
Properties:
  [SubnetIds](#cfn-ec2-transitgatewayattachment-subnetids): 
    - String
  [Tags](#cfn-ec2-transitgatewayattachment-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [TransitGatewayId](#cfn-ec2-transitgatewayattachment-transitgatewayid): String
  [VpcId](#cfn-ec2-transitgatewayattachment-vpcid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayattachment-properties"></a>

`SubnetIds`  <a name="cfn-ec2-transitgatewayattachment-subnetids"></a>
The IDs of one or more subnets\. You can specify only one subnet per Availability Zone\. You must specify at least one subnet, but we recommend that you specify two subnets for better availability\. The transit gateway uses one IP address from each specified subnet\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-ec2-transitgatewayattachment-tags"></a>
The tags to apply to the VPC attachment\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayId`  <a name="cfn-ec2-transitgatewayattachment-transitgatewayid"></a>
The ID of the transit gateway\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VpcId`  <a name="cfn-ec2-transitgatewayattachment-vpcid"></a>
The ID of the VPC\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgatewayattachment-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgatewayattachment-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGatewayAttachment` resource to the intrinsic `Ref` function, the function returns the ID of the attachment, such as `tgw-attach-vpc-0d39e0d39e0d39e`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ec2-transitgatewayattachment-seealso"></a>
+ [CreateTransitGatewayVpcAttachment](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayVpcAttachment.html) in the *Amazon EC2 API Reference*
+ [ModifyTransitGatewayVpcAttachment](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyTransitGatewayVpcAttachment.html) in the *Amazon EC2 API Reference*