# AWS::AppStream::AppBlock S3Location<a name="aws-properties-appstream-appblock-s3location"></a>

The S3 location of the app block\.

## Syntax<a name="aws-properties-appstream-appblock-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-appblock-s3location-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-appstream-appblock-s3location-s3bucket)" : String,
  "[S3Key](#cfn-appstream-appblock-s3location-s3key)" : String
}
```

### YAML<a name="aws-properties-appstream-appblock-s3location-syntax.yaml"></a>

```
  [S3Bucket](#cfn-appstream-appblock-s3location-s3bucket): String
  [S3Key](#cfn-appstream-appblock-s3location-s3key): String
```

## Properties<a name="aws-properties-appstream-appblock-s3location-properties"></a>

`S3Bucket`  <a name="cfn-appstream-appblock-s3location-s3bucket"></a>
The S3 bucket of the app block\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Key`  <a name="cfn-appstream-appblock-s3location-s3key"></a>
The S3 key of the S3 object of the virtual hard disk\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)