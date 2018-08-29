# AWS::EC2::NetworkAcl<a name="aws-resource-ec2-network-acl"></a>

Creates a new network ACL in a VPC\.

**Topics**
+ [Syntax](#aws-resource-ec2-networkacl-syntax)
+ [Properties](#w3ab2c21c10d428b9)
+ [Return Values](#w3ab2c21c10d428c11)
+ [Example](#w3ab2c21c10d428c13)
+ [See Also](#w3ab2c21c10d428c15)

## Syntax<a name="aws-resource-ec2-networkacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkacl-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::NetworkAcl",
   "Properties" : {
      "[Tags](#cfn-ec2-networkacl-tags)" : [ Resource Tag, ... ],
      "[VpcId](#cfn-ec2-networkacl-vpcid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-networkacl-syntax.yaml"></a>

```
Type: "AWS::EC2::NetworkAcl"
Properties:
  [Tags](#cfn-ec2-networkacl-tags):
    - Resource Tag
  [VpcId](#cfn-ec2-networkacl-vpcid): String
```

## Properties<a name="w3ab2c21c10d428b9"></a>

`Tags`  <a name="cfn-ec2-networkacl-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this ACL\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`VpcId`  <a name="cfn-ec2-networkacl-vpcid"></a>
The ID of the VPC where the network ACL will be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d428c11"></a>

### Ref<a name="w3ab2c21c10d428c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d428c13"></a>

### JSON<a name="aws-resource-ec2-networkacl-syntax-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myNetworkAcl" : {
         "Type" : "AWS::EC2::NetworkAcl",
         "Properties" : {
            "VpcId" : { "Ref" : "myVPC" },
            "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-networkacl-syntax-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myNetworkAcl:
    Type: AWS::EC2::NetworkAcl
    Properties:
      VpcId:
        Ref: myVPC
      Tags:
      - Key: foo
        Value: bar
```

## See Also<a name="w3ab2c21c10d428c15"></a>
+ [CreateNetworkAcl](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateNetworkAcl.html) in the *Amazon EC2 API Reference*
+ [Network ACLs](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_ACLs.html) in the *Amazon Virtual Private Cloud User Guide*\.