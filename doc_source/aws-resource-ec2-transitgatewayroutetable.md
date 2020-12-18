# AWS::EC2::TransitGatewayRouteTable<a name="aws-resource-ec2-transitgatewayroutetable"></a>

Specifies a route table for a transit gateway\.

## Syntax<a name="aws-resource-ec2-transitgatewayroutetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroutetable-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRouteTable",
  "Properties" : {
      "[Tags](#cfn-ec2-transitgatewayroutetable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-transitgatewayroutetable-transitgatewayid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroutetable-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayRouteTable
Properties: 
  [Tags](#cfn-ec2-transitgatewayroutetable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-transitgatewayroutetable-transitgatewayid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetable-properties"></a>

`Tags`  <a name="cfn-ec2-transitgatewayroutetable-tags"></a>
Any tags assigned to the route table\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayId`  <a name="cfn-ec2-transitgatewayroutetable-transitgatewayid"></a>
The ID of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayroutetable-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetable-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway route table\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-transitgatewayroutetable--seealso"></a>
+  [CreateTransitGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayRouteTable.html) in the *Amazon EC2 API Reference*

