# AWS::DataSync::Task S3<a name="aws-properties-datasync-task-s3"></a>

Specifies the Amazon S3 bucket where DataSync uploads your [task report](https://docs.aws.amazon.com/datasync/latest/userguide/creating-task-reports.html)\.

## Syntax<a name="aws-properties-datasync-task-s3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-s3-syntax.json"></a>

```
{
  "[BucketAccessRoleArn](#cfn-datasync-task-s3-bucketaccessrolearn)" : String,
  "[S3BucketArn](#cfn-datasync-task-s3-s3bucketarn)" : String,
  "[Subdirectory](#cfn-datasync-task-s3-subdirectory)" : String
}
```

### YAML<a name="aws-properties-datasync-task-s3-syntax.yaml"></a>

```
  [BucketAccessRoleArn](#cfn-datasync-task-s3-bucketaccessrolearn): String
  [S3BucketArn](#cfn-datasync-task-s3-s3bucketarn): String
  [Subdirectory](#cfn-datasync-task-s3-subdirectory): String
```

## Properties<a name="aws-properties-datasync-task-s3-properties"></a>

`BucketAccessRoleArn`  <a name="cfn-datasync-task-s3-bucketaccessrolearn"></a>
Specifies the Amazon Resource Name \(ARN\) of the IAM policy that allows DataSync to upload a task report to your S3 bucket\. For more information, see [Allowing DataSync to upload a task report to an Amazon S3 bucket](https://docs.aws.amazon.com/datasync/latest/userguide/creating-task-reports.html)\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):iam::[0-9]{12}:role/.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketArn`  <a name="cfn-datasync-task-s3-s3bucketarn"></a>
Specifies the ARN of the S3 bucket where DataSync uploads your report\.  
*Required*: No  
*Type*: String  
*Maximum*: `156`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):(s3|s3-outposts):[a-z\-0-9]*:[0-9]*:.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subdirectory`  <a name="cfn-datasync-task-s3-subdirectory"></a>
Specifies a bucket prefix for your report\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\p{Zs}]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)