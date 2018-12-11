# AWS::EC2::TransitGatewayRouteTable<a name="aws-resource-ec2-transitgatewayroutetable"></a>

Creates a route table for a transit gateway\. For more information, see [Amazon VPC Transit Gateways](https://docs.aws.amazon.com/vpc/latest/tgw/)\.

**Topics**
+ [Syntax](#aws-resource-ec2-transitgatewayroutetable-syntax)
+ [Properties](#aws-resource-ec2-transitgatewayroutetable-properties)
+ [Return Values](#aws-resource-ec2-transitgatewayroutetable-returnvalues)
+ [See Also](#aws-resource-ec2-transitgatewayroutetable-seealso)

## Syntax<a name="aws-resource-ec2-transitgatewayroutetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroutetable-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRouteTable",
  "Properties" : {
    "[Tags](#cfn-ec2-transitgatewayroutetable-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[TransitGatewayId](#cfn-ec2-transitgatewayroutetable-transitgatewayid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroutetable-syntax.yaml"></a>

```
Type: "AWS::EC2::TransitGatewayRouteTable"
Properties:
  [Tags](#cfn-ec2-transitgatewayroutetable-tags): 
    - [*Tag*](aws-properties-resource-tags.md)  
  [TransitGatewayId](#cfn-ec2-transitgatewayroutetable-transitgatewayid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetable-properties"></a>

`Tags`  <a name="cfn-ec2-transitgatewayroutetable-tags"></a>
The tags to apply to the transit gateway route table\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TransitGatewayId`  <a name="cfn-ec2-transitgatewayroutetable-transitgatewayid"></a>
The ID of the transit gateway\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-transitgatewayroutetable-returnvalues"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetable-ref"></a>

When you pass the logical ID of an `AWS::EC2::TransitGatewayRouteTable` resource to the intrinsic `Ref` function, the function returns the ID of the transit gateway route table, such as `tgw-rtb-020b99a6568edc33a`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-ec2-transitgatewayroutetable-seealso"></a>
+ [CreateTransitGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayRouteTable.html) in the *Amazon EC2 API Reference*