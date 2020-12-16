# AWS::EC2::TransitGatewayRouteTablePropagation<a name="aws-resource-ec2-transitgatewayroutetablepropagation"></a>

Enables the specified attachment to propagate routes to the specified propagation route table\.

For more information about enabling transit gateway route propagation, see [EnableVgwRoutePropagation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EnableTransitGatewayRouteTablePropagation.html) in the *Amazon Elastic Compute Cloud API Reference*\.

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
Type: AWS::EC2::TransitGatewayRouteTablePropagation
Properties: 
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetablepropagation-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetablepropagation-properties"></a>

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroutetablepropagation-transitgatewayattachmentid"></a>
The ID of the attachment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroutetablepropagation-transitgatewayroutetableid"></a>
The ID of the propagation route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayroutetablepropagation-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetablepropagation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway route table that is propagated\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-transitgatewayroutetablepropagation--seealso"></a>
+  [EnableTransitGatewayRouteTablePropagation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EnableTransitGatewayRouteTablePropagation.html) in the *Amazon Elastic Compute Cloud API Reference* 

