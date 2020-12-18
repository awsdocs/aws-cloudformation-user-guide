# AWS::EC2::NetworkAcl<a name="aws-resource-ec2-network-acl"></a>

Specifies a network ACL for your VPC\.

## Syntax<a name="aws-resource-ec2-network-acl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-network-acl-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkAcl",
  "Properties" : {
      "[Tags](#cfn-ec2-networkacl-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-networkacl-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-network-acl-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkAcl
Properties: 
  [Tags](#cfn-ec2-networkacl-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-networkacl-vpcid): String
```

## Properties<a name="aws-resource-ec2-network-acl-properties"></a>

`Tags`  <a name="cfn-ec2-networkacl-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this ACL\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-networkacl-vpcid"></a>
The ID of the VPC for the network ACL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-network-acl-return-values"></a>

### Ref<a name="aws-resource-ec2-network-acl-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-network-acl--examples"></a>



### Network ACL<a name="aws-resource-ec2-network-acl--examples--Network_ACL"></a>

The following example creates a Network ACL in a VPC\.

#### JSON<a name="aws-resource-ec2-network-acl--examples--Network_ACL--json"></a>

```
"myNetworkAcl" : {
   "Type" : "AWS::EC2::NetworkAcl",
   "Properties" : {
      "VpcId" : { "Ref" : "myVPC" },
      "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
   }
}
```

#### YAML<a name="aws-resource-ec2-network-acl--examples--Network_ACL--yaml"></a>

```
   myNetworkAcl:
      Type: AWS::EC2::NetworkAcl
      Properties:
         VpcId:
           Ref: myVPC
         Tags:
         - Key: foo
           Value: bar
```

## See also<a name="aws-resource-ec2-network-acl--seealso"></a>
+ [CreateNetworkAcl](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateNetworkAcl.html) in the *Amazon EC2 API Reference*
+ [Network ACLs](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_ACLs.html) in the *Amazon Virtual Private Cloud User Guide*

