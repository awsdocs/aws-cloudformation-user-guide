# AWS::EC2::SubnetNetworkAclAssociation<a name="aws-resource-ec2-subnet-network-acl-assoc"></a>

Associates a subnet with a network ACL\. For more information, see [ReplaceNetworkAclAssociation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-ReplaceNetworkAclAssociation.html) in the *Amazon Elastic Compute Cloud API Reference*\.

When `AWS::EC2::SubnetNetworkAclAssociation` resources are created during create or update operations, AWS CloudFormation adopts existing resources that share the same key properties \(the properties that contribute to uniquely identify the resource\)\. However, if the operation fails and rolls back, AWS CloudFormation deletes the previously out\-of\-band resources\. You can protect against this behavior by using `Retain` deletion policies\. For more information, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

## Syntax<a name="aws-resource-ec2-subnet-network-acl-assoc-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnet-network-acl-assoc-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SubnetNetworkAclAssociation",
  "Properties" : {
      "[NetworkAclId](#cfn-ec2-subnetnetworkaclassociation-networkaclid)" : String,
      "[SubnetId](#cfn-ec2-subnetnetworkaclassociation-associationid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-subnet-network-acl-assoc-syntax.yaml"></a>

```
Type: AWS::EC2::SubnetNetworkAclAssociation
Properties: 
  [NetworkAclId](#cfn-ec2-subnetnetworkaclassociation-networkaclid): String
  [SubnetId](#cfn-ec2-subnetnetworkaclassociation-associationid): String
```

## Properties<a name="aws-resource-ec2-subnet-network-acl-assoc-properties"></a>

`NetworkAclId`  <a name="cfn-ec2-subnetnetworkaclassociation-networkaclid"></a>
The ID of the network ACL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-subnetnetworkaclassociation-associationid"></a>
The ID of the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-subnet-network-acl-assoc-return-values"></a>

### Ref<a name="aws-resource-ec2-subnet-network-acl-assoc-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the subnet network ACL association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-subnet-network-acl-assoc-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-subnet-network-acl-assoc-return-values-fn--getatt-fn--getatt"></a>

`AssociationId`  <a name="AssociationId-fn::getatt"></a>
Returns the value of this object's [SubnetId](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-network-acl-assoc.html) property\.

## Examples<a name="aws-resource-ec2-subnet-network-acl-assoc--examples"></a>



### Subnet Network ACL Association<a name="aws-resource-ec2-subnet-network-acl-assoc--examples--Subnet_Network_ACL_Association"></a>

The following example associates subnet mySubnet with the myNetworkAcl network ACL\.

#### JSON<a name="aws-resource-ec2-subnet-network-acl-assoc--examples--Subnet_Network_ACL_Association--json"></a>

```
"mySubnetNetworkAclAssociation" : {
   "Type" : "AWS::EC2::SubnetNetworkAclAssociation",
   "Properties" : {
      "SubnetId" : { "Ref" : "mySubnet" },
      "NetworkAclId" : { "Ref" : "myNetworkAcl" }
   }
}
```

#### YAML<a name="aws-resource-ec2-subnet-network-acl-assoc--examples--Subnet_Network_ACL_Association--yaml"></a>

```
   mySubnetNetworkAclAssociation:
     Type: AWS::EC2::SubnetNetworkAclAssociation
     Properties:
       SubnetId:
         Ref: mySubnet
       NetworkAclId:
         Ref: myNetworkAcl
```