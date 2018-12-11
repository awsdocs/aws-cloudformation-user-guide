# AWS::EC2::TransitGatewayRouteTableAssociation<a name="aws-resource-ec2-transitgatewayroutetableassociation"></a>

Associate an attachment with a transit gateway route table\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgatewayroutetableassociation-syntax)
+ [Properties](#aws-resource-ec2-transitgatewayroutetableassociation-properties)
+ [Return Values](#aws-resource-ec2-transitgatewayroutetableassociation-returnvalues)
+ [See Also](#aws-resource-ec2-transitgatewayroutetableassociation-seealso)

## Syntax<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRouteTableAssociation",
  "Properties" : {
    "[TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid)" : String,
    "[TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGatewayRouteTableAssociation"
Properties:
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetableassociation-properties"></a>

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid"></a>
The ID of the attachment\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid"></a>
The ID of the transit gateway route table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgatewayroutetableassociation-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetableassociation-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGatewayRouteTableAssociation` resource to the intrinsic `Ref` function, the function returns the ID of the attachment and the ID of the transit gateway route table, separated by an underscore, such as `tgw-attach-0bbfdd70ef7d35f5d_tgw-rtb-020b99a6568edc33a`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ec2-transitgatewayroutetableassociation-seealso"></a>
+ [AssociateTransitGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateTransitGatewayRouteTable.html) in the *Amazon EC2 API Reference*