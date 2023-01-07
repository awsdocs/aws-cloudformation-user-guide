# AWS::EC2::VPCPeeringConnection<a name="aws-resource-ec2-vpcpeeringconnection"></a>

Requests a VPC peering connection between two VPCs: a requester VPC that you own and an accepter VPC with which to create the connection\. The accepter VPC can belong to another AWS account and can be in a different Region to the requester VPC\.

The requester VPC and accepter VPC cannot have overlapping CIDR blocks\. If you create a VPC peering connection request between VPCs with overlapping CIDR blocks, the VPC peering connection has a status of `failed`\.

For more information, see [Walkthough: Peer with a VPC in another AWS account](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/peer-with-vpc-in-another-account.html)\.

## Syntax<a name="aws-resource-ec2-vpcpeeringconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcpeeringconnection-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCPeeringConnection",
  "Properties" : {
      "[PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid)" : String,
      "[PeerRegion](#cfn-ec2-vpcpeeringconnection-peerregion)" : String,
      "[PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn)" : String,
      "[PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid)" : String,
      "[Tags](#cfn-ec2-vpcpeeringconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-vpcpeeringconnection-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpcpeeringconnection-syntax.yaml"></a>

```
Type: AWS::EC2::VPCPeeringConnection
Properties: 
  [PeerOwnerId](#cfn-ec2-vpcpeeringconnection-peerownerid): String
  [PeerRegion](#cfn-ec2-vpcpeeringconnection-peerregion): String
  [PeerRoleArn](#cfn-ec2-vpcpeeringconnection-peerrolearn): String
  [PeerVpcId](#cfn-ec2-vpcpeeringconnection-peervpcid): String
  [Tags](#cfn-ec2-vpcpeeringconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-vpcpeeringconnection-vpcid): String
```

## Properties<a name="aws-resource-ec2-vpcpeeringconnection-properties"></a>

`PeerOwnerId`  <a name="cfn-ec2-vpcpeeringconnection-peerownerid"></a>
The AWS account ID of the owner of the accepter VPC\.  
Default: Your AWS account ID  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerRegion`  <a name="cfn-ec2-vpcpeeringconnection-peerregion"></a>
The Region code for the accepter VPC, if the accepter VPC is located in a Region other than the Region in which you make the request\.  
Default: The Region in which you make the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerRoleArn`  <a name="cfn-ec2-vpcpeeringconnection-peerrolearn"></a>
The Amazon Resource Name \(ARN\) of the VPC peer role for the peering connection in another AWS account\.  
This is required when you are peering a VPC in a different AWS account\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerVpcId`  <a name="cfn-ec2-vpcpeeringconnection-peervpcid"></a>
The ID of the VPC with which you are creating the VPC peering connection\. You must specify this parameter in the request\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-vpcpeeringconnection-tags"></a>
Any tags assigned to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-vpcpeeringconnection-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpcpeeringconnection-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcpeeringconnection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC peering connection\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-vpcpeeringconnection--seealso"></a>
+ [What is VPC peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html) in *VPC Peering Guide*
+ [CreateVpcPeeringConnection](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcPeeringConnection.html) in the *Amazon EC2 API Reference*

