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

## Return Values<a name="aws-resource-ec2-transitgatewayroutetable-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetable-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-ec2-transitgatewayroutetable--seealso"></a>
+  [CreateTransitGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayRouteTable.html) in the *Amazon EC2 API Reference*

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
