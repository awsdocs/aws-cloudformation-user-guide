# AWS::EC2::LocalGatewayRoute<a name="aws-resource-ec2-localgatewayroute"></a>

Creates a static route for the specified local gateway route table\. You must specify one of the following targets: 
+  `LocalGatewayVirtualInterfaceGroupId` 
+  `NetworkInterfaceId` 

## Syntax<a name="aws-resource-ec2-localgatewayroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-localgatewayroute-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LocalGatewayRoute",
  "Properties" : {
      "[DestinationCidrBlock](#cfn-ec2-localgatewayroute-destinationcidrblock)" : String,
      "[LocalGatewayRouteTableId](#cfn-ec2-localgatewayroute-localgatewayroutetableid)" : String,
      "[LocalGatewayVirtualInterfaceGroupId](#cfn-ec2-localgatewayroute-localgatewayvirtualinterfacegroupid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-localgatewayroute-networkinterfaceid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-localgatewayroute-syntax.yaml"></a>

```
Type: AWS::EC2::LocalGatewayRoute
Properties: 
  [DestinationCidrBlock](#cfn-ec2-localgatewayroute-destinationcidrblock): String
  [LocalGatewayRouteTableId](#cfn-ec2-localgatewayroute-localgatewayroutetableid): String
  [LocalGatewayVirtualInterfaceGroupId](#cfn-ec2-localgatewayroute-localgatewayvirtualinterfacegroupid): String
  [NetworkInterfaceId](#cfn-ec2-localgatewayroute-networkinterfaceid): String
```

## Properties<a name="aws-resource-ec2-localgatewayroute-properties"></a>

`DestinationCidrBlock`  <a name="cfn-ec2-localgatewayroute-destinationcidrblock"></a>
The CIDR block used for destination matches\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalGatewayRouteTableId`  <a name="cfn-ec2-localgatewayroute-localgatewayroutetableid"></a>
The ID of the local gateway route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalGatewayVirtualInterfaceGroupId`  <a name="cfn-ec2-localgatewayroute-localgatewayvirtualinterfacegroupid"></a>
The ID of the virtual interface group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-localgatewayroute-networkinterfaceid"></a>
The ID of the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-localgatewayroute-return-values"></a>

### Ref<a name="aws-resource-ec2-localgatewayroute-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the local gateway route table and its destination address range\. For example: 

 `{ "Ref": "lgw-rtb-12346789abcdef|10.0.0.0/24" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-localgatewayroute-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-localgatewayroute-return-values-fn--getatt-fn--getatt"></a>

`State`  <a name="State-fn::getatt"></a>
The state of the local gateway route table\.

`Type`  <a name="Type-fn::getatt"></a>
The type of local gateway route\.

## See also<a name="aws-resource-ec2-localgatewayroute--seealso"></a>
+ [Local gateway](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-local-gateways.html) in *AWS Outposts User Guide*
+ [CreateLocalGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLocalGatewayRoute.html) in the *Amazon EC2 API Reference*

