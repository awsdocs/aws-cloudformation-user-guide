# AWS::EC2::LocalGatewayRouteTableVPCAssociation<a name="aws-resource-ec2-localgatewayroutetablevpcassociation"></a>

Associates the specified VPC with the specified local gateway route table\.

## Syntax<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LocalGatewayRouteTableVPCAssociation",
  "Properties" : {
      "[LocalGatewayRouteTableId](#cfn-ec2-localgatewayroutetablevpcassociation-localgatewayroutetableid)" : String,
      "[Tags](#cfn-ec2-localgatewayroutetablevpcassociation-tags)" : Tags,
      "[VpcId](#cfn-ec2-localgatewayroutetablevpcassociation-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-syntax.yaml"></a>

```
Type: AWS::EC2::LocalGatewayRouteTableVPCAssociation
Properties: 
  [LocalGatewayRouteTableId](#cfn-ec2-localgatewayroutetablevpcassociation-localgatewayroutetableid): String
  [Tags](#cfn-ec2-localgatewayroutetablevpcassociation-tags): 
    Tags
  [VpcId](#cfn-ec2-localgatewayroutetablevpcassociation-vpcid): String
```

## Properties<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-properties"></a>

`LocalGatewayRouteTableId`  <a name="cfn-ec2-localgatewayroutetablevpcassociation-localgatewayroutetableid"></a>
The ID of the local gateway route table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-localgatewayroutetablevpcassociation-tags"></a>
The tags assigned to the association\.  
*Required*: No  
*Type*: [Tags](aws-properties-ec2-localgatewayroutetablevpcassociation-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-localgatewayroutetablevpcassociation-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-ec2-localgatewayroutetablevpcassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-localgatewayroutetablevpcassociation-return-values-fn--getatt-fn--getatt"></a>

`LocalGatewayId`  <a name="LocalGatewayId-fn::getatt"></a>
The ID of the local gateway\.

`LocalGatewayRouteTableVpcAssociationId`  <a name="LocalGatewayRouteTableVpcAssociationId-fn::getatt"></a>
The ID of the association\.

`State`  <a name="State-fn::getatt"></a>
The state of the association\.

## See also<a name="aws-resource-ec2-localgatewayroutetablevpcassociation--seealso"></a>
+ [Local Gateways](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-local-gateways.html) in *AWS Outposts User Guide*
+ [CreateLocalGatewayRouteTableVpcAssociation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLocalGatewayRouteTableVpcAssociation.html) in the *Amazon EC2 API Reference*

