# AWS::Athena::WorkGroup AclConfiguration<a name="aws-properties-athena-workgroup-aclconfiguration"></a>

Indicates that an Amazon S3 canned ACL should be set to control ownership of stored query results\. When Athena stores query results in Amazon S3, the canned ACL is set with the `x-amz-acl` request header\. For more information about S3 Object Ownership, see [Object Ownership settings](https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html#object-ownership-overview) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-athena-workgroup-aclconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-aclconfiguration-syntax.json"></a>

```
{
  "[S3AclOption](#cfn-athena-workgroup-aclconfiguration-s3acloption)" : String
}
```

### YAML<a name="aws-properties-athena-workgroup-aclconfiguration-syntax.yaml"></a>

```
  [S3AclOption](#cfn-athena-workgroup-aclconfiguration-s3acloption): String
```

## Properties<a name="aws-properties-athena-workgroup-aclconfiguration-properties"></a>

`S3AclOption`  <a name="cfn-athena-workgroup-aclconfiguration-s3acloption"></a>
The Amazon S3 canned ACL that Athena should specify when storing query results\. Currently the only supported canned ACL is `BUCKET_OWNER_FULL_CONTROL`\. If a query runs in a workgroup and the workgroup overrides client\-side settings, then the Amazon S3 canned ACL specified in the workgroup's settings is used for all queries that run in the workgroup\. For more information about Amazon S3 canned ACLs, see [Canned ACL](https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html#canned-acl) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BUCKET_OWNER_FULL_CONTROL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)