# AWS::S3ObjectLambda::AccessPoint PolicyStatus<a name="aws-properties-s3objectlambda-accesspoint-policystatus"></a>

Indicates whether this access point policy is public\. For more information about how Amazon S3 evaluates policies to determine whether they are public, see [The Meaning of "Public"](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status) in the *Amazon S3 User Guide*\. 

## Syntax<a name="aws-properties-s3objectlambda-accesspoint-policystatus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3objectlambda-accesspoint-policystatus-syntax.json"></a>

```
{
  "[IsPublic](#cfn-s3objectlambda-accesspoint-policystatus-ispublic)" : Boolean
}
```

### YAML<a name="aws-properties-s3objectlambda-accesspoint-policystatus-syntax.yaml"></a>

```
  [IsPublic](#cfn-s3objectlambda-accesspoint-policystatus-ispublic): Boolean
```

## Properties<a name="aws-properties-s3objectlambda-accesspoint-policystatus-properties"></a>

`IsPublic`  <a name="cfn-s3objectlambda-accesspoint-policystatus-ispublic"></a>
  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)