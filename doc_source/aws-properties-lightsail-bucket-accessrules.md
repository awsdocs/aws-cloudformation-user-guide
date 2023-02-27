# AWS::Lightsail::Bucket AccessRules<a name="aws-properties-lightsail-bucket-accessrules"></a>

`AccessRules` is a property of the [AWS::Lightsail::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-bucket.html) resource\. It describes access rules for a bucket\.

## Syntax<a name="aws-properties-lightsail-bucket-accessrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-bucket-accessrules-syntax.json"></a>

```
{
  "[AllowPublicOverrides](#cfn-lightsail-bucket-accessrules-allowpublicoverrides)" : Boolean,
  "[GetObject](#cfn-lightsail-bucket-accessrules-getobject)" : String
}
```

### YAML<a name="aws-properties-lightsail-bucket-accessrules-syntax.yaml"></a>

```
  [AllowPublicOverrides](#cfn-lightsail-bucket-accessrules-allowpublicoverrides): Boolean
  [GetObject](#cfn-lightsail-bucket-accessrules-getobject): String
```

## Properties<a name="aws-properties-lightsail-bucket-accessrules-properties"></a>

`AllowPublicOverrides`  <a name="cfn-lightsail-bucket-accessrules-allowpublicoverrides"></a>
A Boolean value indicating whether the access control list \(ACL\) permissions that are applied to individual objects override the `GetObject` option that is currently specified\.  
When this is true, you can use the [PutObjectAcl](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObjectAcl.html) Amazon S3 API operation to set individual objects to public \(read\-only\) or private, using either the `public-read` ACL or the `private` ACL\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GetObject`  <a name="cfn-lightsail-bucket-accessrules-getobject"></a>
Specifies the anonymous access to all objects in a bucket\.  
The following options can be specified:  
+  `public` \- Sets all objects in the bucket to public \(read\-only\), making them readable by everyone on the internet\.

  If the `GetObject` value is set to `public`, then all objects in the bucket default to public regardless of the `allowPublicOverrides` value\.
+  `private` \- Sets all objects in the bucket to private, making them readable only by you and anyone that you grant access to\.

  If the `GetObject` value is set to `private`, and the `allowPublicOverrides` value is set to `true`, then all objects in the bucket default to private unless they are configured with a `public-read` ACL\. Individual objects with a `public-read` ACL are readable by everyone on the internet\.
*Required*: No  
*Type*: String  
*Allowed values*: `private | public`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)