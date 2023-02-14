# AWS::MSK::Cluster S3<a name="aws-properties-msk-cluster-s3"></a>

The details of the Amazon S3 destination for broker logs\.

## Syntax<a name="aws-properties-msk-cluster-s3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-s3-syntax.json"></a>

```
{
  "[Bucket](#cfn-msk-cluster-s3-bucket)" : String,
  "[Enabled](#cfn-msk-cluster-s3-enabled)" : Boolean,
  "[Prefix](#cfn-msk-cluster-s3-prefix)" : String
}
```

### YAML<a name="aws-properties-msk-cluster-s3-syntax.yaml"></a>

```
  [Bucket](#cfn-msk-cluster-s3-bucket): String
  [Enabled](#cfn-msk-cluster-s3-enabled): Boolean
  [Prefix](#cfn-msk-cluster-s3-prefix): String
```

## Properties<a name="aws-properties-msk-cluster-s3-properties"></a>

`Bucket`  <a name="cfn-msk-cluster-s3-bucket"></a>
The name of the S3 bucket that is the destination for broker logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-msk-cluster-s3-enabled"></a>
Specifies whether broker logs get sent to the specified Amazon S3 destination\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-msk-cluster-s3-prefix"></a>
The S3 prefix that is the destination for broker logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)