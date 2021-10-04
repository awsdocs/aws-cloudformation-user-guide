# AWS::FSx::FileSystem AuditLogConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration"></a>

The configuration that Amazon FSx for Windows File Server uses to audit and log user accesses of files, folders, and file shares on the Amazon FSx for Windows File Server file system\. For more information, see [ File access auditing](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/file-access-auditing.html)\.

**Note**  
File access auditing is supported only on Amazon FSx for Windows File Server file systems with a throughput capacity of 32 MB/s or greater\.

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
The Amazon Resource Name \(ARN\) that specifies the destination of the audit event logs\.  
The destination can be any Amazon CloudWatch Logs log group ARN or Amazon Kinesis Data Firehose delivery stream ARN, with the following requirements:  
+ The destination ARN that you provide \(either CloudWatch Logs log group or Kinesis Data Firehose delivery stream\) must be in the same AWS partition, AWS Region, and AWS account as your Amazon FSx file system\.
+ The name of the CloudWatch Logs log group must begin with the `/aws/fsx/` prefix\. The name of the Kinesis Data Firehose delivery stream must begin with the `aws-fsx-` prefix\.
+ If you do not provide a destination in `AuditLogDestination`, Amazon FSx will create and use a log stream in the CloudWatch Logs `/aws/fsx/windows` log group\.
+ If `AuditLogDestination` is provided and the resource does not exist, the request will fail with a `BadRequest` error\.
+ If `FileAccessAuditLogLevel` and `FileShareAccessAuditLogLevel` are both set to `DISABLED`, you cannot specify a destination in `AuditLogDestination`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileAccessAuditLogLevel`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileaccessauditloglevel"></a>
Sets which attempt type is logged by Amazon FSx for end\-user accesses of files and folders\.  
+ `SUCCESS_ONLY` \- only successful attempts to access files or folders are logged\.
+ `FAILURE_ONLY` \- only failed attempts to access files or folders are logged\.
+ `SUCCESS_AND_FAILURE` \- both successful attempts and failed attempts to access files or folders are logged\.
+ `DISABLED` \- access auditing of files and folders is turned off\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileShareAccessAuditLogLevel`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration-fileshareaccessauditloglevel"></a>
Sets which attempt type is logged by Amazon FSx for end\-user accesses of file shares\.  
+ `SUCCESS_ONLY` \- only successful attempts to access file shares are logged\.
+ `FAILURE_ONLY` \- only failed attempts to access file shares are logged\.
+ `SUCCESS_AND_FAILURE` \- both successful attempts and failed attempts to access file shares are logged\.
+ `DISABLED` \- access auditing of file shares is turned off\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)