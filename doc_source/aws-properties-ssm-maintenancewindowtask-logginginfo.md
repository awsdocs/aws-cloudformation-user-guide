# Amazon EC2 Systems Manager MaintenanceWindowTask LoggingInfo<a name="aws-properties-ssm-maintenancewindowtask-logginginfo"></a>

<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-description"></a>The `LoggingInfo` property type specifies information about the Amazon S3 bucket to write instance\-level logs to\.

<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-inheritance"></a> `LoggingInfo` is a property of the [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md) resource\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket)" : String,
  "[Region](#cfn-ssm-maintenancewindowtask-logginginfo-region)" : String,
  "[S3Prefix](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.yaml"></a>

```
[S3Bucket](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket): String
[Region](#cfn-ssm-maintenancewindowtask-logginginfo-region): String
[S3Prefix](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-properties"></a>

`S3Bucket`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-s3bucket"></a>
The name of the Amazon S3 bucket where execution logs are stored\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Region`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-region"></a>
The region where the Amazon S3 bucket is located\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Prefix`  <a name="cfn-ssm-maintenancewindowtask-logginginfo-s3prefix"></a>
The Amazon S3 bucket subfolder\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 