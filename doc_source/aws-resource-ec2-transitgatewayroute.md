# AWS::EC2::TransitGatewayRoute<a name="aws-resource-ec2-transitgatewayroute"></a>

Specifies a static route for a transit gateway route table\.

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
Type: AWS::EC2::TransitGatewayRoute
Properties: 
  [Blackhole](#cfn-ec2-transitgatewayroute-blackhole): Boolean
  [DestinationCidrBlock](#cfn-ec2-transitgatewayroute-destinationcidrblock): String
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroute-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroute-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroute-properties"></a>

`Blackhole`  <a name="cfn-ec2-transitgatewayroute-blackhole"></a>
Indicates whether to drop traffic that matches this route\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationCidrBlock`  <a name="cfn-ec2-transitgatewayroute-destinationcidrblock"></a>
The CIDR block used for destination matches\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroute-transitgatewayattachmentid"></a>
The ID of the attachment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroute-transitgatewayroutetableid"></a>
The ID of the transit gateway route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayroute-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroute-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway route\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-transitgatewayroute--seealso"></a>
+  [CreateTransitGatewayRoute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayRoute.html) in the *Amazon EC2 API Reference*

