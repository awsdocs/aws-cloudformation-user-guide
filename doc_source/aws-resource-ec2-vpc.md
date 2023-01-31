# AWS::EC2::VPC<a name="aws-resource-ec2-vpc"></a>

Specifies a virtual private cloud \(VPC\)\.

You can optionally request an IPv6 CIDR block for the VPC\. You can request an Amazon\-provided IPv6 CIDR block from Amazon's pool of IPv6 addresses, or an IPv6 CIDR block from an IPv6 address pool that you provisioned through bring your own IP addresses \(BYOIP\)\.

For more information, see [Virtual private clouds \(VPC\)](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/configure-your-vpc.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-vpc-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpc-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPC",
  "Properties" : {
      "[CidrBlock](#cfn-ec2-vpc-cidrblock)" : String,
      "[EnableDnsHostnames](#cfn-ec2-vpc-enablednshostnames)" : Boolean,
      "[EnableDnsSupport](#cfn-ec2-vpc-enablednssupport)" : Boolean,
      "[InstanceTenancy](#cfn-ec2-vpc-instancetenancy)" : String,
      "[Ipv4IpamPoolId](#cfn-ec2-vpc-ipv4ipampoolid)" : String,
      "[Ipv4NetmaskLength](#cfn-ec2-vpc-ipv4netmasklength)" : Integer,
      "[Tags](#cfn-ec2-vpc-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-vpc-syntax.yaml"></a>

```
Type: AWS::EC2::VPC
Properties: 
  [CidrBlock](#cfn-ec2-vpc-cidrblock): String
  [EnableDnsHostnames](#cfn-ec2-vpc-enablednshostnames): Boolean
  [EnableDnsSupport](#cfn-ec2-vpc-enablednssupport): Boolean
  [InstanceTenancy](#cfn-ec2-vpc-instancetenancy): String
  [Ipv4IpamPoolId](#cfn-ec2-vpc-ipv4ipampoolid): String
  [Ipv4NetmaskLength](#cfn-ec2-vpc-ipv4netmasklength): Integer
  [Tags](#cfn-ec2-vpc-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-vpc-properties"></a>

`CidrBlock`  <a name="cfn-ec2-vpc-cidrblock"></a>
The IPv4 network range for the VPC, in CIDR notation\. For example, `10.0.0.0/16`\. We modify the specified CIDR block to its canonical form; for example, if you specify `100.68.0.18/18`, we modify it to `100.68.0.0/18`\.  
You must specify either`CidrBlock` or `Ipv4IpamPoolId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableDnsHostnames`  <a name="cfn-ec2-vpc-enablednshostnames"></a>
Indicates whether the instances launched in the VPC get DNS hostnames\. If enabled, instances in the VPC get DNS hostnames; otherwise, they do not\. Disabled by default for nondefault VPCs\. For more information, see [DNS attributes in your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-dns.html#vpc-dns-support)\.  
You can only enable DNS hostnames if you've enabled DNS support\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableDnsSupport`  <a name="cfn-ec2-vpc-enablednssupport"></a>
Indicates whether the DNS resolution is supported for the VPC\. If enabled, queries to the Amazon provided DNS server at the 169\.254\.169\.253 IP address, or the reserved IP address at the base of the VPC network range "plus two" succeed\. If disabled, the Amazon provided DNS service in the VPC that resolves public DNS hostnames to IP addresses is not enabled\. Enabled by default\. For more information, see [DNS attributes in your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-dns.html#vpc-dns-support)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceTenancy`  <a name="cfn-ec2-vpc-instancetenancy"></a>
The allowed tenancy of instances launched into the VPC\.  
+ `default`: An instance launched into the VPC runs on shared hardware by default, unless you explicitly specify a different tenancy during instance launch\.
+ `dedicated`: An instance launched into the VPC runs on dedicated hardware by default, unless you explicitly specify a tenancy of `host` during instance launch\. You cannot specify a tenancy of `default` during instance launch\.
Updating `InstanceTenancy` requires no replacement only if you are updating its value from `dedicated` to `default`\. Updating `InstanceTenancy` from `default` to `dedicated` requires replacement\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default | host`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Ipv4IpamPoolId`  <a name="cfn-ec2-vpc-ipv4ipampoolid"></a>
The ID of an IPv4 IPAM pool you want to use for allocating this VPC's CIDR\. For more information, see [What is IPAM?](/vpc/latest/ipam/what-is-it-ipam.html) in the *Amazon VPC IPAM User Guide*\.  
You must specify either`CidrBlock` or `Ipv4IpamPoolId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ipv4NetmaskLength`  <a name="cfn-ec2-vpc-ipv4netmasklength"></a>
The netmask length of the IPv4 CIDR you want to allocate to this VPC from an Amazon VPC IP Address Manager \(IPAM\) pool\. For more information about IPAM, see [What is IPAM?](https://docs.aws.amazon.com/vpc/latest/ipam/what-is-it-ipam.html) in the *Amazon VPC IPAM User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-vpc-tags"></a>
The tags for the VPC\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-vpc-return-values"></a>

### Ref<a name="aws-resource-ec2-vpc-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-vpc-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-vpc-return-values-fn--getatt-fn--getatt"></a>

`CidrBlock`  <a name="CidrBlock-fn::getatt"></a>
The primary IPv4 CIDR block for the VPC\. For example, 10\.0\.0\.0/16\.

`CidrBlockAssociations`  <a name="CidrBlockAssociations-fn::getatt"></a>
The association IDs of the IPv4 CIDR blocks for the VPC\. For example, \[ vpc\-cidr\-assoc\-0280ab6b \]\.

`DefaultNetworkAcl`  <a name="DefaultNetworkAcl-fn::getatt"></a>
The ID of the default network ACL for the VPC\. For example, acl\-814dafe3\.

`DefaultSecurityGroup`  <a name="DefaultSecurityGroup-fn::getatt"></a>
The ID of the default security group for the VPC\. For example, sg\-b178e0d3\.

`Ipv6CidrBlocks`  <a name="Ipv6CidrBlocks-fn::getatt"></a>
The IPv6 CIDR blocks for the VPC\. For example, \[ 2001:db8:1234:1a00::/56 \]\.

`VpcId`  <a name="VpcId-fn::getatt"></a>
The ID of the VPC\.

## Examples<a name="aws-resource-ec2-vpc--examples"></a>



### VPC<a name="aws-resource-ec2-vpc--examples--VPC"></a>

The following example specifies a VPC with an IPv4 address\. For an example with IPv6 enabled, see [Creating an IPv6 enabled VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-cidr.html#intrinsic-function-reference-cidr-example2)\.

#### JSON<a name="aws-resource-ec2-vpc--examples--VPC--json"></a>

```
"myVPC" : {
   "Type" : "AWS::EC2::VPC",
   "Properties" : {
      "CidrBlock" : "10.0.0.0/16",
      "EnableDnsSupport" : "true",
      "EnableDnsHostnames" : "true",
      "Tags" : [ 
         {"Key" : "stack", "Value" : "production"} 
      ]
   }
}
```

#### YAML<a name="aws-resource-ec2-vpc--examples--VPC--yaml"></a>

```
myVPC:
  Type: AWS::EC2::VPC
  Properties:
    CidrBlock: 10.0.0.0/16
    EnableDnsSupport: 'true'
    EnableDnsHostnames: 'true'
    Tags:
     - Key: stack
       Value: production
```

## See also<a name="aws-resource-ec2-vpc--seealso"></a>
+  [CreateVpc](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpc.html) in the *Amazon EC2 API Reference*
+  [VPC and subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon VPC User Guide*

