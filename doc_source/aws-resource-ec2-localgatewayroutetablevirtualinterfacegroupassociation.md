# AWS::EC2::LocalGatewayRouteTableVirtualInterfaceGroupAssociation<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation"></a>

Describes an association between a local gateway route table and a virtual interface group\.

## Syntax<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LocalGatewayRouteTableVirtualInterfaceGroupAssociation",
  "Properties" : {
      "[LocalGatewayRouteTableId](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayroutetableid)" : String,
      "[LocalGatewayVirtualInterfaceGroupId](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayvirtualinterfacegroupid)" : String,
      "[Tags](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-syntax.yaml"></a>

```
Type: AWS::EC2::LocalGatewayRouteTableVirtualInterfaceGroupAssociation
Properties: 
  [LocalGatewayRouteTableId](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayroutetableid): String
  [LocalGatewayVirtualInterfaceGroupId](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayvirtualinterfacegroupid): String
  [Tags](#cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-properties"></a>

`LocalGatewayRouteTableId`  <a name="cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayroutetableid"></a>
The ID of the local gateway route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalGatewayVirtualInterfaceGroupId`  <a name="cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-localgatewayvirtualinterfacegroupid"></a>
The ID of the virtual interface group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-localgatewayroutetablevirtualinterfacegroupassociation-tags"></a>
The tags assigned to the association\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the local gateway route table virtual interface group association\. For example: 

 `{ "Ref": "lgw-vif-grp-assoc-07145b276bEXAMPLE" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation-return-values-fn--getatt-fn--getatt"></a>

`LocalGatewayId`  <a name="LocalGatewayId-fn::getatt"></a>
The ID of the local gateway\.

`LocalGatewayRouteTableArn`  <a name="LocalGatewayRouteTableArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the local gateway route table for the virtual interface group\.

`LocalGatewayRouteTableVirtualInterfaceGroupAssociationId`  <a name="LocalGatewayRouteTableVirtualInterfaceGroupAssociationId-fn::getatt"></a>
The ID of the association\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The ID of the AWS account that owns the local gateway virtual interface group association\.

`State`  <a name="State-fn::getatt"></a>
The state of the association\.

## See also<a name="aws-resource-ec2-localgatewayroutetablevirtualinterfacegroupassociation--seealso"></a>
+ [Local gateway](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-local-gateways.html) in *AWS Outposts User Guide*
+ [CreateLocalGatewayRouteTableVirtualInterfaceGroupAssociation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLocalGatewayRouteTableVirtualInterfaceGroupAssociation.html) in the *Amazon EC2 API Reference*

