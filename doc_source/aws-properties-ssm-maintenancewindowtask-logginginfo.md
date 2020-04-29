# AWS::SSM::MaintenanceWindowTask LoggingInfo<a name="aws-properties-ssm-maintenancewindowtask-logginginfo"></a>

The `LoggingInfo` property type specifies information about the Amazon S3 bucket to write instance\-level logs to\.

 `LoggingInfo` is a property of the [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) resource\.

**Note**  
 `LoggingInfo` has been deprecated\. To specify an S3 bucket to contain logs, instead use the `OutputS3BucketName` and `OutputS3KeyPrefix` options in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported maintenance window task types, see [AWS Systems Manager MaintenanceWindowTask TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html)\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.json"></a>

```
{
  "[Region](#cfn-ssm-maintenancewindowtask-logginginfo-region)" : String,
  "[S3Bucket](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket)" : String,
  "[S3Prefix](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.yaml"></a>

```
  [Region](#cfn-ssm-maintenancewindowtask-logginginfo-region): String
  [S3Bucket](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket): String
  [S3Prefix](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-properties"></a>

`Region`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-region"></a>
The Region where the S3 bucket is located\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-s3bucket"></a>
The name of an S3 bucket where execution logs are stored \.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Prefix`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-s3prefix"></a>
The Amazon S3 bucket subfolder\.   
*Required*: No  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)