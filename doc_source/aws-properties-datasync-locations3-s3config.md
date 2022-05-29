# AWS::DataSync::LocationS3 S3Config<a name="aws-properties-datasync-locations3-s3config"></a>

The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role used to access an Amazon S3 bucket\.

For detailed information about using such a role, see [Creating a Location for Amazon S3](https://docs.aws.amazon.com/datasync/latest/userguide/working-with-locations.html#create-s3-location) in the * AWS DataSync User Guide*\.

## Syntax<a name="aws-properties-datasync-locations3-s3config-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locations3-s3config-syntax.json"></a>

```
{
  "[BucketAccessRoleArn](#cfn-datasync-locations3-s3config-bucketaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-datasync-locations3-s3config-syntax.yaml"></a>

```
  [BucketAccessRoleArn](#cfn-datasync-locations3-s3config-bucketaccessrolearn): String
```

## Properties<a name="aws-properties-datasync-locations3-s3config-properties"></a>

`BucketAccessRoleArn`  <a name="cfn-datasync-locations3-s3config-bucketaccessrolearn"></a>
The ARN of the IAM role for accessing the S3 bucket\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):iam::[0-9]{12}:role/.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)