# AWS::EC2::SubnetNetworkAclAssociation<a name="aws-resource-ec2-subnet-network-acl-assoc"></a>

Associates a subnet with a network ACL\. For more information, see [ReplaceNetworkAclAssociation](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-ReplaceNetworkAclAssociation.html) in the *Amazon EC2 API Reference*\.

When `AWS::EC2::SubnetNetworkAclAssociation` resources are created during create or update operations, AWS CloudFormation adopts existing resources that share the same key properties \(the properties that contribute to uniquely identify the resource\)\. However, if the operation fails and rolls back, AWS CloudFormation deletes the previously out\-of\-band resources\. You can protect against this behavior by using `Retain` deletion policies\. For more information, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

**Note**  
The EC2 API Reference refers to the `SubnetId` parameter as the `AssociationId`\.

**Topics**
+ [Syntax](#aws-resource-ec2-subnetnetworkaclassociation-syntax)
+ [Properties](#w3ab2c21c10d493c13)
+ [Return Values](#w3ab2c21c10d493c15)
+ [Template Examples](#w3ab2c21c10d493c17)

## Syntax<a name="aws-resource-ec2-subnetnetworkaclassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-subnetnetworkaclassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SubnetNetworkAclAssociation",
  "Properties" : {
    "[SubnetId](#cfn-ec2-subnetnetworkaclassociation-associationid)" : String,
    "[NetworkAclId](#cfn-ec2-subnetnetworkaclassociation-networkaclid)" : String
  }
}
```

### YAML<a name="aws-resource-subnetnetworkaclassociation-syntax.yaml"></a>

```
Type: "AWS::EC2::SubnetNetworkAclAssociation"
Properties:
  [SubnetId](#cfn-ec2-subnetnetworkaclassociation-associationid): String
  [NetworkAclId](#cfn-ec2-subnetnetworkaclassociation-networkaclid): String
```

## Properties<a name="w3ab2c21c10d493c13"></a>

`SubnetId`  <a name="cfn-ec2-subnetnetworkaclassociation-associationid"></a>
The ID representing the current association between the original network ACL and the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NetworkAclId`  <a name="cfn-ec2-subnetnetworkaclassociation-networkaclid"></a>
The ID of the new ACL to associate with the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d493c15"></a>

### Ref<a name="w3ab2c21c10d493c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d493c15b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`AssociationId`  
Returns the value of this object's [SubnetId](#cfn-ec2-subnetnetworkaclassociation-associationid) property\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Template Examples<a name="w3ab2c21c10d493c17"></a>

### JSON<a name="aws-resource-subnetnetworkaclassociation-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "mySubnetNetworkAclAssociation" : {
         "Type" : "AWS::EC2::SubnetNetworkAclAssociation",
         "Properties" : {
            "SubnetId" : { "Ref" : "mySubnet" },
            "NetworkAclId" : { "Ref" : "myNetworkAcl" }
         }
      }
   }
}
```

### YAML<a name="aws-resource-subnetnetworkaclassociation-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  mySubnetNetworkAclAssociation:
    Type: AWS::EC2::SubnetNetworkAclAssociation
    Properties:
      SubnetId:
        Ref: mySubnet
      NetworkAclId:
        Ref: myNetworkAcl
```