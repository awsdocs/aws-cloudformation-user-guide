# AWS::CodeBuild::Project LogsConfig<a name="aws-properties-codebuild-project-logsconfig"></a>

 `LogsConfig` is a property of the [AWS CodeBuild Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html) resource that specifies information about logs for a build project\. These can be logs in Amazon CloudWatch Logs, built in a specified S3 bucket, or both\. 

## Syntax<a name="aws-properties-codebuild-project-logsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-logsconfig-syntax.json"></a>

```
{
  "[CloudWatchLogs](#cfn-codebuild-project-logsconfig-cloudwatchlogs)" : CloudWatchLogsConfig,
  "[S3Logs](#cfn-codebuild-project-logsconfig-s3logs)" : S3LogsConfig
}
```

### YAML<a name="aws-properties-codebuild-project-logsconfig-syntax.yaml"></a>

```
  [CloudWatchLogs](#cfn-codebuild-project-logsconfig-cloudwatchlogs): 
    CloudWatchLogsConfig
  [S3Logs](#cfn-codebuild-project-logsconfig-s3logs): 
    S3LogsConfig
```

## Properties<a name="aws-properties-codebuild-project-logsconfig-properties"></a>

`CloudWatchLogs`  <a name="cfn-codebuild-project-logsconfig-cloudwatchlogs"></a>
 Information about Amazon CloudWatch Logs for a build project\. Amazon CloudWatch Logs are enabled by default\.   
*Required*: No  
*Type*: [CloudWatchLogsConfig](aws-properties-codebuild-project-cloudwatchlogsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Logs`  <a name="cfn-codebuild-project-logsconfig-s3logs"></a>
 Information about logs built to an S3 bucket for a build project\. S3 logs are not enabled by default\.   
*Required*: No  
*Type*: [S3LogsConfig](aws-properties-codebuild-project-s3logsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-codebuild-project-logsconfig--seealso"></a>
+  [ LogsConfig](https://docs.aws.amazon.com/codebuild/latest/APIReference/API_LogsConfig.html) in the *AWS CodeBuild API Reference* 