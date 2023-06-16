# AWS::EC2::InstanceConnectEndpoint<a name="aws-resource-ec2-instanceconnectendpoint"></a>

Creates an EC2 Instance Connect Endpoint\.

An EC2 Instance Connect Endpoint allows you to connect to an instance, without requiring the instance to have a public IPv4 address\. For more information, see [Connect to your instances without requiring a public IPv4 address using EC2 Instance Connect Endpoint](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Connect-using-EC2-Instance-Connect-Endpoint.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-resource-ec2-instanceconnectendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-instanceconnectendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::InstanceConnectEndpoint",
  "Properties" : {
      "[ClientToken](#cfn-ec2-instanceconnectendpoint-clienttoken)" : String,
      "[PreserveClientIp](#cfn-ec2-instanceconnectendpoint-preserveclientip)" : Boolean,
      "[SecurityGroupIds](#cfn-ec2-instanceconnectendpoint-securitygroupids)" : [ String, ... ],
      "[SubnetId](#cfn-ec2-instanceconnectendpoint-subnetid)" : String,
      "[Tags](#cfn-ec2-instanceconnectendpoint-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-instanceconnectendpoint-syntax.yaml"></a>

```
Type: AWS::EC2::InstanceConnectEndpoint
Properties: 
  [ClientToken](#cfn-ec2-instanceconnectendpoint-clienttoken): String
  [PreserveClientIp](#cfn-ec2-instanceconnectendpoint-preserveclientip): Boolean
  [SecurityGroupIds](#cfn-ec2-instanceconnectendpoint-securitygroupids): 
    - String
  [SubnetId](#cfn-ec2-instanceconnectendpoint-subnetid): String
  [Tags](#cfn-ec2-instanceconnectendpoint-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-instanceconnectendpoint-properties"></a>

`ClientToken`  <a name="cfn-ec2-instanceconnectendpoint-clienttoken"></a>
Unique, case\-sensitive identifier that you provide to ensure the idempotency of the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreserveClientIp`  <a name="cfn-ec2-instanceconnectendpoint-preserveclientip"></a>
Indicates whether your client's IP address is preserved as the source\. The value is `true` or `false`\.  
+ If `true`, your client's IP address is used when you connect to a resource\.
+ If `false`, the elastic network interface IP address is used when you connect to a resource\.
Default: `true`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupIds`  <a name="cfn-ec2-instanceconnectendpoint-securitygroupids"></a>
One or more security groups to associate with the endpoint\. If you don't specify a security group, the default security group for your VPC will be associated with the endpoint\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-instanceconnectendpoint-subnetid"></a>
The ID of the subnet in which to create the EC2 Instance Connect Endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-instanceconnectendpoint-tags"></a>
The tags to apply to the EC2 Instance Connect Endpoint during creation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-instanceconnectendpoint-return-values"></a>

### Ref<a name="aws-resource-ec2-instanceconnectendpoint-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-ec2-instanceconnectendpoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-instanceconnectendpoint-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the EC2 Instance Connect Endpoint\.