# AWS::EC2::EIP<a name="aws-properties-ec2-eip"></a>

Specifies an Elastic IP \(EIP\) address and can, optionally, associate it with an Amazon EC2 instance\.

You can allocate an Elastic IP address from an address pool owned by AWS or from an address pool created from a public IPv4 address range that you have brought to AWS for use with your AWS resources using bring your own IP addresses \(BYOIP\)\. For more information, see [Bring Your Own IP Addresses \(BYOIP\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-byoip.html) in the *Amazon Elastic Compute Cloud User Guide*\.

\[EC2\-VPC\] If you release an Elastic IP address, you might be able to recover it\. You cannot recover an Elastic IP address that you released after it is allocated to another AWS account\. You cannot recover an Elastic IP address for EC2\-Classic\. To attempt to recover an Elastic IP address that you released, specify it in this operation\.

An Elastic IP address is for use either in the EC2\-Classic platform or in a VPC\. By default, you can allocate 5 Elastic IP addresses for EC2\-Classic per Region and 5 Elastic IP addresses for EC2\-VPC per Region\.

For more information, see [Elastic IP Addresses](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) in the *Amazon Elastic Compute Cloud User Guide*\.

## Syntax<a name="aws-properties-ec2-eip-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-eip-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EIP",
  "Properties" : {
      "[Domain](#cfn-ec2-eip-domain)" : String,
      "[InstanceId](#cfn-ec2-eip-instanceid)" : String,
      "[PublicIpv4Pool](#cfn-ec2-eip-publicipv4pool)" : String,
      "[Tags](#cfn-ec2-eip-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-properties-ec2-eip-syntax.yaml"></a>

```
Type: AWS::EC2::EIP
Properties: 
  [Domain](#cfn-ec2-eip-domain): String
  [InstanceId](#cfn-ec2-eip-instanceid): String
  [PublicIpv4Pool](#cfn-ec2-eip-publicipv4pool): String
  [Tags](#cfn-ec2-eip-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-eip-properties"></a>

`Domain`  <a name="cfn-ec2-eip-domain"></a>
Indicates whether the Elastic IP address is for use with instances in a VPC or instance in EC2\-Classic\.  
Default: If the Region supports EC2\-Classic, the default is `standard`\. Otherwise, the default is `vpc`\.  
Use when allocating an address for use with a VPC if the Region supports EC2\-Classic\.  
If you define an Elastic IP address and associate it with a VPC that is defined in the same template, you must declare a dependency on the VPC\-gateway attachment by using the [ DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) on this resource\.  
*Required*: No  
*Type*: String  
*Allowed values*: `standard | vpc`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-ec2-eip-instanceid"></a>
The ID of the instance\.  
Updates to the `InstanceId` property may require *some interruptions*\. Updates on an EIP reassociates the address on its associated resource\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PublicIpv4Pool`  <a name="cfn-ec2-eip-publicipv4pool"></a>
The ID of an address pool that you own\. Use this parameter to let Amazon EC2 select an address from the address pool\.  
Updates to the `PublicIpv4Pool` property may require *some interruptions*\. Updates on an EIP reassociates the address on its associated resource\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Tags`  <a name="cfn-ec2-eip-tags"></a>
Any tags assigned to the Elastic IP address\.  
Updates to the `Tags` property may require *some interruptions*\. Updates on an EIP reassociates the address on its associated resource\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-eip-return-values"></a>

### Ref<a name="aws-properties-ec2-eip-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Elastic IP address\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-ec2-eip-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-ec2-eip-return-values-fn--getatt-fn--getatt"></a>

`AllocationId`  <a name="AllocationId-fn::getatt"></a>
The ID that AWS assigns to represent the allocation of the address for use with Amazon VPC\. This is returned only for VPC elastic IP addresses\. For example, `eipalloc-5723d13e`\.

## Examples<a name="aws-properties-ec2-eip--examples"></a>

### Allocating an Amazon EC2 Elastic IP Using AWS::EC2::EIP\.<a name="aws-properties-ec2-eip--examples--Allocating_an_Amazon_EC2_Elastic_IP_Using_AWS::EC2::EIP."></a>

This example shows how to allocate an Amazon EC2 Elastic IP address and assign it to an Amazon EC2 instance using a [ AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html) resource\.

#### JSON<a name="aws-properties-ec2-eip--examples--Allocating_an_Amazon_EC2_Elastic_IP_Using_AWS::EC2::EIP.--json"></a>

```
"MyEIP" : {
  "Type" : "AWS::EC2::EIP",
  "Properties" : {
    "InstanceId" : { "Ref" : "logical name of an AWS::EC2::Instance resource" }
  }
}
```

#### YAML<a name="aws-properties-ec2-eip--examples--Allocating_an_Amazon_EC2_Elastic_IP_Using_AWS::EC2::EIP.--yaml"></a>

```
MyEIP:
  Type: AWS::EC2::EIP
  Properties:
    InstanceId: !Ref Logical name of an AWS::EC2::Instance resource
```