# AWS::S3::AccessPoint PolicyStatus<a name="aws-properties-s3-accesspoint-policystatus"></a>

The container element for a bucket's policy status\.

## Syntax<a name="aws-properties-s3-accesspoint-policystatus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-accesspoint-policystatus-syntax.json"></a>

```
{
  "[IsPublic](#cfn-s3-accesspoint-policystatus-ispublic)" : String
}
```

### YAML<a name="aws-properties-s3-accesspoint-policystatus-syntax.yaml"></a>

```
  [IsPublic](#cfn-s3-accesspoint-policystatus-ispublic): String
```

## Properties<a name="aws-properties-s3-accesspoint-policystatus-properties"></a>

`IsPublic`  <a name="cfn-s3-accesspoint-policystatus-ispublic"></a>
The policy status for this bucket\. `TRUE` indicates that this bucket is public\. `FALSE` indicates that the bucket is not public\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)