# AWS::EC2::TransitGatewayRoute<a name="aws-resource-ec2-transitgatewayroute"></a>

Creates a static route for a transit gateway route table\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgatewayroute-syntax)
+ [Properties](#aws-resource-ec2-transitgatewayroute-properties)
+ [Return Values](#aws-resource-ec2-transitgatewayroute-returnvalues)
+ [See Also](#aws-resource-ec2-transitgatewayroute-seealso)

## Syntax<a name="aws-resource-ec2-transitgatewayroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroute-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRoute",
  "Properties" : {
    "[Blackhole](#cfn-ec2-transitgatewayroute-blackhole)" : Boolean,
    "[DestinationCidrBlock](#cfn-ec2-transitgatewayroute-destinationcidrblock)" : String,
    "[TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroute-transitgatewayattachmentid)" : String,
    "[TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroute-transitgatewayroutetableid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroute-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGatewayRoute"
Properties:
  [Blackhole](#cfn-ec2-transitgatewayroute-blackhole): Boolean
  [DestinationCidrBlock](#cfn-ec2-transitgatewayroute-destinationcidrblock): String
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroute-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroute-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroute-properties"></a>

`Blackhole`  <a name="cfn-ec2-transitgatewayroute-blackhole"></a>
Indicates whether to drop traffic if the target isn't available\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DestinationCidrBlock`  <a name="cfn-ec2-transitgatewayroute-destinationcidrblock"></a>
The CIDR range used for destination matches\. Routing decisions are based on the most specific match\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroute-transitgatewayattachmentid"></a>
The ID of the attachment\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroute-transitgatewayroutetableid"></a>
The ID of the transit gateway route table\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgatewayroute-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroute-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGatewayRoute` resource to the intrinsic `Ref` function, the function returns the ID of the route table and the destination CIDR, separated by an underscore, such as `tgw-rtb-0ea209e5dcc99f3a3_0.0.0.0/0`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ec2-transitgatewayroute-seealso"></a>
+ [CreateTransitGatewayRoute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayRoute.html) in the *Amazon EC2 API Reference*