# AWS::EC2::GatewayRouteTableAssociation<a name="aws-resource-ec2-gatewayroutetableassociation"></a>

Associates a virtual private gateway or internet gateway with a route table\. The gateway and route table must be in the same VPC\. This association causes the incoming traffic to the gateway to be routed according to the routes in the route table\.

## Syntax<a name="aws-resource-ec2-gatewayroutetableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-gatewayroutetableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::GatewayRouteTableAssociation",
  "Properties" : {
      "[GatewayId](#cfn-ec2-gatewayroutetableassociation-gatewayid)" : String,
      "[RouteTableId](#cfn-ec2-gatewayroutetableassociation-routetableid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-gatewayroutetableassociation-syntax.yaml"></a>

```
Type: AWS::EC2::GatewayRouteTableAssociation
Properties: 
  [GatewayId](#cfn-ec2-gatewayroutetableassociation-gatewayid): String
  [RouteTableId](#cfn-ec2-gatewayroutetableassociation-routetableid): String
```

## Properties<a name="aws-resource-ec2-gatewayroutetableassociation-properties"></a>

`GatewayId`  <a name="cfn-ec2-gatewayroutetableassociation-gatewayid"></a>
The ID of the gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteTableId`  <a name="cfn-ec2-gatewayroutetableassociation-routetableid"></a>
The ID of the route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-gatewayroutetableassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-gatewayroutetableassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the gateway\.

### Fn::GetAtt<a name="aws-resource-ec2-gatewayroutetableassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-gatewayroutetableassociation-return-values-fn--getatt-fn--getatt"></a>

`AssociationId`  <a name="AssociationId-fn::getatt"></a>
The ID of the route table association\.