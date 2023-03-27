# AWS::EC2::LocalGatewayRouteTable<a name="aws-resource-ec2-localgatewayroutetable"></a>

Describes a local gateway route table\.

## Syntax<a name="aws-resource-ec2-localgatewayroutetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-localgatewayroutetable-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LocalGatewayRouteTable",
  "Properties" : {
      "[LocalGatewayId](#cfn-ec2-localgatewayroutetable-localgatewayid)" : String,
      "[Mode](#cfn-ec2-localgatewayroutetable-mode)" : String,
      "[Tags](#cfn-ec2-localgatewayroutetable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-localgatewayroutetable-syntax.yaml"></a>

```
Type: AWS::EC2::LocalGatewayRouteTable
Properties: 
  [LocalGatewayId](#cfn-ec2-localgatewayroutetable-localgatewayid): String
  [Mode](#cfn-ec2-localgatewayroutetable-mode): String
  [Tags](#cfn-ec2-localgatewayroutetable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-localgatewayroutetable-properties"></a>

`LocalGatewayId`  <a name="cfn-ec2-localgatewayroutetable-localgatewayid"></a>
The ID of the local gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-ec2-localgatewayroutetable-mode"></a>
The mode of the local gateway route table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `coip | direct-vpc-routing`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-localgatewayroutetable-tags"></a>
The tags assigned to the local gateway route table\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-localgatewayroutetable-return-values"></a>

### Ref<a name="aws-resource-ec2-localgatewayroutetable-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the local gateway route table\. For example: 

 `{ "Ref": "lgw-rtb-059615ef7deEXAMPLE" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-localgatewayroutetable-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-localgatewayroutetable-return-values-fn--getatt-fn--getatt"></a>

`LocalGatewayRouteTableArn`  <a name="LocalGatewayRouteTableArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the local gateway route table\.

`LocalGatewayRouteTableId`  <a name="LocalGatewayRouteTableId-fn::getatt"></a>
The ID of the local gateway route table\.

`OutpostArn`  <a name="OutpostArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The ID of the AWS account that owns the local gateway route table\.

`State`  <a name="State-fn::getatt"></a>
The state of the local gateway route table\.

## See also<a name="aws-resource-ec2-localgatewayroutetable--seealso"></a>
+ [Local gateway](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-local-gateways.html) in *AWS Outposts User Guide*
+ [CreateLocalGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLocalGatewayRoute.html) in the *Amazon EC2 API Reference*

