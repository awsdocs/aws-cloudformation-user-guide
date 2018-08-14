# AWS::EC2::VPC<a name="aws-resource-ec2-vpc"></a>

Creates a Virtual Private Cloud \(VPC\) with the CIDR block that you specify\. To name a VPC resource, use the `Tags` property and specify a value for the `Name` key\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpc-syntax)
+ [Properties](#w3ab2c21c10d511b9)
+ [Return Values](#w3ab2c21c10d511c11)
+ [Example](#w3ab2c21c10d511c13)
+ [More Info](#w3ab2c21c10d511c15)

## Syntax<a name="aws-resource-ec2-vpc-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpc-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPC",
   "Properties" : {
      "[CidrBlock](#cfn-aws-ec2-vpc-cidrblock)" : String,
      "[EnableDnsSupport](#cfn-aws-ec2-vpc-EnableDnsSupport)" : Boolean,
      "[EnableDnsHostnames](#cfn-aws-ec2-vpc-EnableDnsHostnames)" : Boolean,
      "[InstanceTenancy](#cfn-aws-ec2-vpc-instancetenancy)" : String,
      "[Tags](#cfn-aws-ec2-vpc-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-vpc-syntax.yaml"></a>

```
Type: "AWS::EC2::VPC"
Properties: 
  [CidrBlock](#cfn-aws-ec2-vpc-cidrblock): String
  [EnableDnsSupport](#cfn-aws-ec2-vpc-EnableDnsSupport): Boolean
  [EnableDnsHostnames](#cfn-aws-ec2-vpc-EnableDnsHostnames): Boolean
  [InstanceTenancy](#cfn-aws-ec2-vpc-instancetenancy): String
  [Tags](#cfn-aws-ec2-vpc-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d511b9"></a>

`CidrBlock`  <a name="cfn-aws-ec2-vpc-cidrblock"></a>
The CIDR block you want the VPC to cover\. For example: `"10.0.0.0/16"`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EnableDnsSupport`  <a name="cfn-aws-ec2-vpc-EnableDnsSupport"></a>
Specifies whether DNS resolution is supported for the VPC\. If this attribute is `true`, the Amazon DNS server resolves DNS hostnames for your instances to their corresponding IP addresses; otherwise, it does not\. By default the value is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EnableDnsHostnames`  <a name="cfn-aws-ec2-vpc-EnableDnsHostnames"></a>
Specifies whether the instances launched in the VPC get DNS hostnames\. If this attribute is `true`, instances in the VPC get DNS hostnames; otherwise, they do not\. You can only set `EnableDnsHostnames` to `true` if you also set the `EnableDnsSupport` attribute to `true`\. By default, the value is set to `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceTenancy`  <a name="cfn-aws-ec2-vpc-instancetenancy"></a>
The allowed tenancy of instances launched into the VPC\.   
+ `"default"`: Instances can be launched with any tenancy\.
+ `"dedicated"`: Any instance launched into the VPC automatically has dedicated tenancy, unless you launch it with the default tenancy\.
Update: Conditional\. Updating `InstanceTenancy` requires no replacement only if you are updating its value from `"dedicated"` to `"default"`\. Updating `InstanceTenancy` from `"default"` to `"dedicated"` requires replacement\.  
*Required*: No  
*Type*: String  
*Valid values*: `"default"` or `"dedicated"`  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-aws-ec2-vpc-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this VPC\. To name a VPC resource, specify a value for the `Name` key\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

## Return Values<a name="w3ab2c21c10d511c11"></a>

### Ref<a name="w3ab2c21c10d511c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID, such as `vpc-18ac277d`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d511c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`CidrBlock`  
The set of IP addresses for the VPC\. For example, `10.0.0.0/16`\.

`CidrBlockAssociations`  
A list of IPv4 CIDR block association IDs for the VPC\. For example, `[ vpc-cidr-assoc-0280ab6b ]`\.

`DefaultNetworkAcl`  
The default network ACL ID that is associated with the VPC\. For example, `acl-814dafe3`\.

`DefaultSecurityGroup`  
The default security group ID that is associated with the VPC\. For example, `sg-b178e0d3`\.

`Ipv6CidrBlocks`  
A list of IPv6 CIDR blocks that are associated with the VPC, such as `[ 2001:db8:1234:1a00::/56 ]`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d511c13"></a>

### JSON<a name="aws-resource-ec2-vpc-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myVPC" : {
         "Type" : "AWS::EC2::VPC",
         "Properties" : {
            "CidrBlock" : "10.0.0.0/16",
    	    "EnableDnsSupport" : "false",
    	    "EnableDnsHostnames" : "false",
            "InstanceTenancy" : "dedicated",
            "Tags" : [ {"Key" : "foo", "Value" : "bar"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-vpc-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsSupport: 'false'
      EnableDnsHostnames: 'false'
      InstanceTenancy: dedicated
      Tags:
      - Key: foo
        Value: bar
```

## More Info<a name="w3ab2c21c10d511c15"></a>
+ [CreateVpc](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpc.html) in the *Amazon EC2 API Reference*\.