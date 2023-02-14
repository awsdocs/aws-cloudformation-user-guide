# AWS::MemoryDB::ACL<a name="aws-resource-memorydb-acl"></a>

Specifies an Access Control List\. For more information, see [Authenticating users with Access Contol Lists \(ACLs\)](https://docs.aws.amazon.com/memorydb/latest/devguide/clusters.acls.html)\.

## Syntax<a name="aws-resource-memorydb-acl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-memorydb-acl-syntax.json"></a>

```
{
  "Type" : "AWS::MemoryDB::ACL",
  "Properties" : {
      "[ACLName](#cfn-memorydb-acl-aclname)" : String,
      "[Tags](#cfn-memorydb-acl-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserNames](#cfn-memorydb-acl-usernames)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-memorydb-acl-syntax.yaml"></a>

```
Type: AWS::MemoryDB::ACL
Properties: 
  [ACLName](#cfn-memorydb-acl-aclname): String
  [Tags](#cfn-memorydb-acl-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserNames](#cfn-memorydb-acl-usernames): 
    - String
```

## Properties<a name="aws-resource-memorydb-acl-properties"></a>

`ACLName`  <a name="cfn-memorydb-acl-aclname"></a>
The name of the Access Control List\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-memorydb-acl-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserNames`  <a name="cfn-memorydb-acl-usernames"></a>
The list of users that belong to the Access Control List\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-memorydb-acl-return-values"></a>

### Fn::GetAtt<a name="aws-resource-memorydb-acl-return-values-fn--getatt"></a>

#### <a name="aws-resource-memorydb-acl-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, Ref returns the ARN of the Access Control List, such as `arn:aws:memorydb:us-east-1:123456789012:acl/my-acl`

`Status`  <a name="Status-fn::getatt"></a>
Indicates ACL status\.  
*Valid values*: `creating` \| `active` \| `modifying` \| `deleting`