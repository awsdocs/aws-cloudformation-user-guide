# AWS::EC2::TransitGatewayAttachment<a name="aws-resource-ec2-transitgatewayattachment"></a>

Attaches a VPC to a transit gateway\.

If you attach a VPC with a CIDR range that overlaps the CIDR range of a VPC that is already attached, the new VPC CIDR range is not propagated to the default propagation route table\.

To send VPC traffic to an attached transit gateway, add a route to the VPC route table using [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)\.

## Syntax<a name="aws-resource-ec2-transitgatewayattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayAttachment",
  "Properties" : {
      "[SubnetIds](#cfn-ec2-transitgatewayattachment-subnetids)" : [ String, ... ],
      "[Tags](#cfn-ec2-transitgatewayattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-transitgatewayattachment-transitgatewayid)" : String,
      "[VpcId](#cfn-ec2-transitgatewayattachment-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayattachment-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayAttachment
Properties: 
  [SubnetIds](#cfn-ec2-transitgatewayattachment-subnetids): 
    - String
  [Tags](#cfn-ec2-transitgatewayattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-transitgatewayattachment-transitgatewayid): String
  [VpcId](#cfn-ec2-transitgatewayattachment-vpcid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayattachment-properties"></a>

`SubnetIds`  <a name="cfn-ec2-transitgatewayattachment-subnetids"></a>
The IDs of one or more subnets\. You can specify only one subnet per Availability Zone\. You must specify at least one subnet, but we recommend that you specify two subnets for better availability\. The transit gateway uses one IP address from each specified subnet\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-transitgatewayattachment-tags"></a>
The tags for the attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayId`  <a name="cfn-ec2-transitgatewayattachment-transitgatewayid"></a>
The ID of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-ec2-transitgatewayattachment-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayattachment-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-transitgatewayattachment--seealso"></a>
+  [CreateTransitGatewayVpcAttachment](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayVpcAttachment.html) in the *Amazon EC2 API Reference*\.
+  [ModifyTransitGatewayVpcAttachment](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyTransitGatewayVpcAttachment.html) in the *Amazon EC2 API Reference*

