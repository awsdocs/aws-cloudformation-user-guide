# AWS::EC2::TransitGatewayVpcAttachment<a name="aws-resource-ec2-transitgatewayvpcattachment"></a>

Specifies a VPC attachment\.

## Syntax<a name="aws-resource-ec2-transitgatewayvpcattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayvpcattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayVpcAttachment",
  "Properties" : {
      "[AddSubnetIds](#cfn-ec2-transitgatewayvpcattachment-addsubnetids)" : [ String, ... ],
      "[Options](#cfn-ec2-transitgatewayvpcattachment-options)" : Options,
      "[RemoveSubnetIds](#cfn-ec2-transitgatewayvpcattachment-removesubnetids)" : [ String, ... ],
      "[SubnetIds](#cfn-ec2-transitgatewayvpcattachment-subnetids)" : [ String, ... ],
      "[Tags](#cfn-ec2-transitgatewayvpcattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-transitgatewayvpcattachment-transitgatewayid)" : String,
      "[VpcId](#cfn-ec2-transitgatewayvpcattachment-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayvpcattachment-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayVpcAttachment
Properties: 
  [AddSubnetIds](#cfn-ec2-transitgatewayvpcattachment-addsubnetids): 
    - String
  [Options](#cfn-ec2-transitgatewayvpcattachment-options): 
    Options
  [RemoveSubnetIds](#cfn-ec2-transitgatewayvpcattachment-removesubnetids): 
    - String
  [SubnetIds](#cfn-ec2-transitgatewayvpcattachment-subnetids): 
    - String
  [Tags](#cfn-ec2-transitgatewayvpcattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-transitgatewayvpcattachment-transitgatewayid): String
  [VpcId](#cfn-ec2-transitgatewayvpcattachment-vpcid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayvpcattachment-properties"></a>

`AddSubnetIds`  <a name="cfn-ec2-transitgatewayvpcattachment-addsubnetids"></a>
The IDs of one or more subnets to add\. You can specify at most one subnet per Availability Zone\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-ec2-transitgatewayvpcattachment-options"></a>
The VPC attachment options, in JSON or YAML\.  
+ `ApplianceModeSupport` \- Set to `enable` or `disable`\. The default is `disable`\.
+ `DnsSupport` \- Set to `enable` or `disable`\. The default is `enable`\.
+ `Ipv6Support` \- Set to `enable` or `disable`\. The default is `disable`\.
*Required*: No  
*Type*: [Options](aws-properties-ec2-transitgatewayvpcattachment-options.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveSubnetIds`  <a name="cfn-ec2-transitgatewayvpcattachment-removesubnetids"></a>
The IDs of one or more subnets to remove\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-ec2-transitgatewayvpcattachment-subnetids"></a>
The IDs of the subnets\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-transitgatewayvpcattachment-tags"></a>
The tags for the VPC attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayId`  <a name="cfn-ec2-transitgatewayvpcattachment-transitgatewayid"></a>
The ID of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-ec2-transitgatewayvpcattachment-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayvpcattachment-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayvpcattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewayvpcattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewayvpcattachment-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the attachment\.