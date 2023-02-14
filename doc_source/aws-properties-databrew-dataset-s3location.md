# AWS::DataBrew::Dataset S3Location<a name="aws-properties-databrew-dataset-s3location"></a>

Represents an Amazon S3 location \(bucket name, bucket owner, and object key\) where DataBrew can read input data, or write output from a job\.

## Syntax<a name="aws-properties-databrew-dataset-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-s3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-databrew-dataset-s3location-bucket)" : String,
  "[Key](#cfn-databrew-dataset-s3location-key)" : String
}
```

### YAML<a name="aws-properties-databrew-dataset-s3location-syntax.yaml"></a>

```
  [Bucket](#cfn-databrew-dataset-s3location-bucket): String
  [Key](#cfn-databrew-dataset-s3location-key): String
```

## Properties<a name="aws-properties-databrew-dataset-s3location-properties"></a>

`Bucket`  <a name="cfn-databrew-dataset-s3location-bucket"></a>
The Amazon S3 bucket name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-databrew-dataset-s3location-key"></a>
The unique name of the object in the bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1280`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)