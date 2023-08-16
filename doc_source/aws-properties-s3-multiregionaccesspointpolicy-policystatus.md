# AWS::S3::MultiRegionAccessPointPolicy PolicyStatus<a name="aws-properties-s3-multiregionaccesspointpolicy-policystatus"></a>

The container element for a bucket's policy status\.

## Syntax<a name="aws-properties-s3-multiregionaccesspointpolicy-policystatus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-multiregionaccesspointpolicy-policystatus-syntax.json"></a>

```
{
  "[IsPublic](#cfn-s3-multiregionaccesspointpolicy-policystatus-ispublic)" : String
}
```

### YAML<a name="aws-properties-s3-multiregionaccesspointpolicy-policystatus-syntax.yaml"></a>

```
  [IsPublic](#cfn-s3-multiregionaccesspointpolicy-policystatus-ispublic): String
```

## Properties<a name="aws-properties-s3-multiregionaccesspointpolicy-policystatus-properties"></a>

`IsPublic`  <a name="cfn-s3-multiregionaccesspointpolicy-policystatus-ispublic"></a>
The policy status for this bucket\. `TRUE` indicates that this bucket is public\. `FALSE` indicates that the bucket is not public\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)