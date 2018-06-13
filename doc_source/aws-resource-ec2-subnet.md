# AWS::EC2::Subnet<a name="aws-resource-ec2-subnet"></a>

Creates a subnet in an existing VPC\.

**Topics**
+ [Syntax](#aws-resource-ec2-subnet-syntax)
+ [Properties](#aws-resource-ec2-subnet-properties)
+ [Return Values](#aws-resource-ec2-subnet-returnvalues)
+ [Example](#aws-resource-ec2-subnet-examples)
+ [More Info](#w3ab2c21c10d484c15)

## Syntax<a name="aws-resource-ec2-subnet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
    "[AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation)" : Boolean,
    "[AvailabilityZone](#cfn-ec2-subnet-availabilityzone)" : String,
    "[CidrBlock](#cfn-ec2-subnet-cidrblock)" : String,
    "[Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock)" : String,
    "[MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch)" : Boolean,
    "[Tags](#cfn-ec2-subnet-tags)" : [ Resource Tag, ... ],
    "[VpcId](#cfn-awsec2subnet-prop-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-subnet-syntax.yaml"></a>

```
Type: "AWS::EC2::Subnet"
Properties:
  [AssignIpv6AddressOnCreation](#cfn-ec2-subnet-assignipv6addressoncreation): Boolean
  [AvailabilityZone](#cfn-ec2-subnet-availabilityzone): String
  [CidrBlock](#cfn-ec2-subnet-cidrblock): String
  [Ipv6CidrBlock](#cfn-ec2-subnet-ipv6cidrblock): String
  [MapPublicIpOnLaunch](#cfn-ec2-subnet-mappubliciponlaunch): Boolean
  [Tags](#cfn-ec2-subnet-tags):
    - Resource Tag
  [VpcId](#cfn-awsec2subnet-prop-vpcid): String
```

## Properties<a name="aws-resource-ec2-subnet-properties"></a>

`AssignIpv6AddressOnCreation`  <a name="cfn-ec2-subnet-assignipv6addressoncreation"></a>
Indicates whether a network interface created in this subnet receives an IPv6 address\. The default value is `false`\.  
*Required*: Conditional\. If you specify a `true` or `false` value for `AssignIpv6AddressOnCreation`, `Ipv6CidrBlock` must also be specified\.  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
If `AssignIpv6AddressOnCreation` is specified, `MapPublicIpOnLaunch` cannot be specified\.

`AvailabilityZone`  <a name="cfn-ec2-subnet-availabilityzone"></a>
The availability zone in which you want the subnet\. Default: AWS selects a zone for you \(recommended\)\.  
*Required*: No  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)   
If you update this property, you must also update the `CidrBlock` property\.

`CidrBlock`  <a name="cfn-ec2-subnet-cidrblock"></a>
The CIDR block that you want the subnet to cover \(for example, `"10.0.0.0/24"`\)\.  
*Required*: Yes  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)   
If you update this property, you must also update the `AvailabilityZone` property\.

`Ipv6CidrBlock`  <a name="cfn-ec2-subnet-ipv6cidrblock"></a>
The IPv6 network range for the subnet, in CIDR notation\. The subnet size must use a `/64` prefix length\.  
*Required*: Conditional\. If you specify a `true` or `false` value for `AssignIpv6AddressOnCreation`, `Ipv6CidrBlock` must be specified\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MapPublicIpOnLaunch`  <a name="cfn-ec2-subnet-mappubliciponlaunch"></a>
Indicates whether instances that are launched in this subnet receive a public IP address\. By default, the value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
If `MapPublicIpOnLaunch` is specified\. `AssignIpv6AddressOnCreation` cannot be specified\.

`Tags`  <a name="cfn-ec2-subnet-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this subnet\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcId`  <a name="cfn-awsec2subnet-prop-vpcid"></a>
A Ref structure that contains the ID of the VPC on which you want to create the subnet\. The VPC ID is provided as the value of the "Ref" property, as: `{ "Ref": "VPCID" }`\.  
*Required*: Yes  
*Type*: Ref ID  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)   
If you update this property, you must also update the `CidrBlock` property\.

## Return Values<a name="aws-resource-ec2-subnet-returnvalues"></a>

You can pass the logical ID of the resource to an intrinsic function to get a value back from the resource\. The value that is returned depends on the function that you used\.

### Ref<a name="aws-resource-ec2-subnet-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID, such as `subnet-e19f0178`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-ec2-subnet-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`AvailabilityZone`  
Returns the availability zone \(for example, "`us-east-1a`"\) of this subnet\.  
Example:  

```
{ "Fn::GetAtt" : [ "mySubnet", "AvailabilityZone" ] } 
```

`Ipv6CidrBlocks`  
A list of IPv6 CIDR blocks that are associated with the subnet, such as `[ 2001:db8:1234:1a00::/64 ]`\.

`NetworkAclAssociationId`  
The ID of the network ACL that is associated with the subnet's VPC, such as `acl-5fb85d36`\.

`VpcId`  
The ID of the subnet's VPC, such as `vpc-11ad4878`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-ec2-subnet-examples"></a>

The following example snippet uses the VPC ID from a VPC named *myVPC* that was declared elsewhere in the same template\.

### JSON<a name="aws-resource-ec2-subnet-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "mySubnet" : {
         "Type" : "AWS::EC2::Subnet",
         "Properties" : {
            "VpcId" : { "Ref" : "myVPC" },
            "CidrBlock" : "10.0.0.0/24",
            "AvailabilityZone" : "us-east-1a",
            "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-subnet-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  mySubnet:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: myVPC
      CidrBlock: 10.0.0.0/24
      AvailabilityZone: "us-east-1a"
      Tags:
      - Key: foo
        Value: bar
```

## More Info<a name="w3ab2c21c10d484c15"></a>
+ [CreateSubnet](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateSubnet.html) in the *Amazon EC2 API Reference*
+ [Using Tags](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*