# AWS::MediaConnect::FlowVpcInterface<a name="aws-resource-mediaconnect-flowvpcinterface"></a>

The AWS::MediaConnect::FlowVpcInterface resource is a connection between your AWS Elemental MediaConnect flow and a virtual private cloud \(VPC\) that you created using the Amazon Virtual Private Cloud service\.

To avoid streaming your content over the public internet, you can add up to two VPC interfaces to your flow and use those connections to transfer content between your VPC and MediaConnect\.

You can update an existing flow to add a VPC interface\. If you haven’t created the flow yet, you must create the flow with a temporary standard source by doing the following:

1. Use CloudFormation to create a flow with a standard source that uses to the flow’s public IP address\.

1. Use CloudFormation to create a VPC interface to add to this flow\. This can also be done as part of the previous step\.

1. After CloudFormation has created the flow and the VPC interface, update the source to point to the VPC interface that you created\.

## Syntax<a name="aws-resource-mediaconnect-flowvpcinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-flowvpcinterface-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::FlowVpcInterface",
  "Properties" : {
      "[FlowArn](#cfn-mediaconnect-flowvpcinterface-flowarn)" : String,
      "[Name](#cfn-mediaconnect-flowvpcinterface-name)" : String,
      "[RoleArn](#cfn-mediaconnect-flowvpcinterface-rolearn)" : String,
      "[SecurityGroupIds](#cfn-mediaconnect-flowvpcinterface-securitygroupids)" : [ String, ... ],
      "[SubnetId](#cfn-mediaconnect-flowvpcinterface-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-mediaconnect-flowvpcinterface-syntax.yaml"></a>

```
Type: AWS::MediaConnect::FlowVpcInterface
Properties: 
  [FlowArn](#cfn-mediaconnect-flowvpcinterface-flowarn): String
  [Name](#cfn-mediaconnect-flowvpcinterface-name): String
  [RoleArn](#cfn-mediaconnect-flowvpcinterface-rolearn): String
  [SecurityGroupIds](#cfn-mediaconnect-flowvpcinterface-securitygroupids): 
    - String
  [SubnetId](#cfn-mediaconnect-flowvpcinterface-subnetid): String
```

## Properties<a name="aws-resource-mediaconnect-flowvpcinterface-properties"></a>

`FlowArn`  <a name="cfn-mediaconnect-flowvpcinterface-flowarn"></a>
The Amazon Resource Name \(ARN\) of the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-mediaconnect-flowvpcinterface-name"></a>
The name of the VPC Interface\. This value must be unique within the current flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-mediaconnect-flowvpcinterface-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that you created when you set up MediaConnect as a trusted service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-mediaconnect-flowvpcinterface-securitygroupids"></a>
The VPC security groups that you want MediaConnect to use for your VPC configuration\. You must include at least one security group in the request\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-mediaconnect-flowvpcinterface-subnetid"></a>
The subnet IDs that you want to use for your VPC interface\.  
A range of IP addresses in your VPC\. When you create your VPC, you specify a range of IPv4 addresses for the VPC in the form of a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\. This is the primary CIDR block for your VPC\. When you create a subnet for your VPC, you specify the CIDR block for the subnet, which is a subset of the VPC CIDR block\.  
The subnets that you use across all VPC interfaces on the flow must be in the same Availability Zone as the flow\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-flowvpcinterface-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-flowvpcinterface-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the flow ARN and the name of the VPC interface\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:flow:1-23aBC45dEF67hiJ8-12AbC34DE5fG:BasketballGame|MyVPCInterface" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-flowvpcinterface-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-flowvpcinterface-return-values-fn--getatt-fn--getatt"></a>

`NetworkInterfaceIds`  <a name="NetworkInterfaceIds-fn::getatt"></a>
The IDs of the network interfaces that MediaConnect created in your account\.