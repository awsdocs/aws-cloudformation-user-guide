# AWS::FSx::FileSystem AuditLogConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration"></a>

The configuration that Amazon FSx for Windows File Server uses to audit and log user accesses of files, folders, and file shares on the Amazon FSx for Windows File Server file system\.

## Syntax<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration-syntax.json"></a>

```
{
  "[AuditLogDestination](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-auditlogdestination)" : String,
  "[FileAccessAuditLogLevel](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileaccessauditloglevel)" : String,
  "[FileShareAccessAuditLogLevel](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileshareaccessauditloglevel)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration-syntax.yaml"></a>

```
  [AuditLogDestination](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-auditlogdestination): String
  [FileAccessAuditLogLevel](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileaccessauditloglevel): String
  [FileShareAccessAuditLogLevel](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileshareaccessauditloglevel): String
```

## Properties<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration-properties"></a>

`AuditLogDestination`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-auditlogdestination"></a>
The Amazon Resource Name \(ARN\) for the destination of the audit logs\. The destination can be any Amazon CloudWatch Logs log group ARN or Amazon Kinesis Data Firehose delivery stream ARN\.  
The name of the Amazon CloudWatch Logs log group must begin with the `/aws/fsx` prefix\. The name of the Amazon Kinesis Data Firehouse delivery stream must begin with the `aws-fsx` prefix\.  
The destination ARN \(either CloudWatch Logs log group or Kinesis Data Firehose delivery stream\) must be in the same AWS partition, AWS Region, and AWS account as your Amazon FSx file system\.  
*Required*: No  
*Type*: String  
*Minimum*: `8`  
*Maximum*: `1024`  
*Pattern*: `^arn:[^:]{1,63}:[^:]{0,63}:[^:]{0,63}:(?:|\d{12}):[^/].{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileAccessAuditLogLevel`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileaccessauditloglevel"></a>
Sets which attempt type is logged by Amazon FSx for file and folder accesses\.  
+  `SUCCESS_ONLY` \- only successful attempts to access files or folders are logged\.
+  `FAILURE_ONLY` \- only failed attempts to access files or folders are logged\.
+  `SUCCESS_AND_FAILURE` \- both successful attempts and failed attempts to access files or folders are logged\.
+  `DISABLED` \- access auditing of files and folders is turned off\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | FAILURE_ONLY | SUCCESS_AND_FAILURE | SUCCESS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileShareAccessAuditLogLevel`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileshareaccessauditloglevel"></a>
Sets which attempt type is logged by Amazon FSx for file share accesses\.  
+  `SUCCESS_ONLY` \- only successful attempts to access file shares are logged\.
+  `FAILURE_ONLY` \- only failed attempts to access file shares are logged\.
+  `SUCCESS_AND_FAILURE` \- both successful attempts and failed attempts to access file shares are logged\.
+  `DISABLED` \- access auditing of file shares is turned off\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | FAILURE_ONLY | SUCCESS_AND_FAILURE | SUCCESS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)