# AWS::EC2::TransitGatewayRouteTablePropagation<a name="aws-resource-ec2-transitgatewayroutetablepropagation"></a>

Enables an attachment to propagate routes\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgatewayroutetablepropagation-syntax)
+ [Properties](#aws-resource-ec2-transitgatewayroutetablepropagation-properties)
+ [Return Values](#aws-resource-ec2-transitgatewayroutetablepropagation-returnvalues)
+ [See Also](#aws-resource-ec2-transitgatewayroutetablepropagation-seealso)

## Syntax<a name="aws-resource-ec2-transitgatewayroutetablepropagation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroutetablepropagation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRouteTablePropagation",
  "Properties" : {
    "[TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayattachmentid)" : String,
    "[TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayroutetableid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroutetablepropagation-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGatewayRouteTablePropagation"
Properties:
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetablepropagation-properties"></a>

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroutetablepropagation-transitgatewayattachmentid"></a>
The ID of the attachment\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroutetablepropagation-transitgatewayroutetableid"></a>
The ID of the propagation route table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgatewayroutetablepropagation-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetablepropagation-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGatewayRouteTablePropagation` resource to the intrinsic `Ref` function, the function returns the ID of the attachment and the ID of the propagation route table, separated by an underscore, such as `tgw-attach-0bbfdd70ef7d35f5d_tgw-rtb-020b99a6568edc33a`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ec2-transitgatewayroutetablepropagation-seealso"></a>
+ [EnableTransitGatewayRouteTablePropagation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EnableTransitGatewayRouteTablePropagation.html) in the *Amazon EC2 API Reference*