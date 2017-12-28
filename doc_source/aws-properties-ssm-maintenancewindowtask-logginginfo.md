# Amazon EC2 Systems Manager MaintenanceWindowTask LoggingInfo<a name="aws-properties-ssm-maintenancewindowtask-logginginfo"></a>

<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-description"></a>The `LoggingInfo` property type specifies information about the Amazon S3 bucket to write instance\-level logs to\.

<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-inheritance"></a> `LoggingInfo` is a property of the [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md) resource\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-region)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-s3bucket): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-region): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo-s3prefix): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-logginginfo-properties"></a>

`S3Bucket`  
The name of the Amazon S3 bucket where execution logs are stored\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Region`  
The region where the Amazon S3 bucket is located\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`S3Prefix`  
The Amazon S3 bucket subfolder\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 