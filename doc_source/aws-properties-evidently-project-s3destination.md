# AWS::Evidently::Project S3Destination<a name="aws-properties-evidently-project-s3destination"></a>

If the project stores evaluation events in an Amazon S3 bucket, this structure stores the bucket name and bucket prefix\.

## Syntax<a name="aws-properties-evidently-project-s3destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-project-s3destination-syntax.json"></a>

```
{
  "[BucketName](#cfn-evidently-project-s3destination-bucketname)" : String,
  "[Prefix](#cfn-evidently-project-s3destination-prefix)" : String
}
```

### YAML<a name="aws-properties-evidently-project-s3destination-syntax.yaml"></a>

```
  [BucketName](#cfn-evidently-project-s3destination-bucketname): String
  [Prefix](#cfn-evidently-project-s3destination-prefix): String
```

## Properties<a name="aws-properties-evidently-project-s3destination-properties"></a>

`BucketName`  <a name="cfn-evidently-project-s3destination-bucketname"></a>
The name of the bucket in which Evidently stores evaluation events\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-evidently-project-s3destination-prefix"></a>
The bucket prefix in which Evidently stores evaluation events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)