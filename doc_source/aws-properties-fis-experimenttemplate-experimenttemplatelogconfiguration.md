# AWS::FIS::ExperimentTemplate ExperimentTemplateLogConfiguration<a name="aws-properties-fis-experimenttemplate-experimenttemplatelogconfiguration"></a>

Specifies the configuration for experiment logging\.

For more information, see [Experiment logging](https://docs.aws.amazon.com/fis/latest/userguide/monitoring-logging.html) in the *AWS Fault Injection Simulator User Guide*\.

## Syntax<a name="aws-properties-fis-experimenttemplate-experimenttemplatelogconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-experimenttemplatelogconfiguration-syntax.json"></a>

```
{
  "[CloudWatchLogsConfiguration](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-cloudwatchlogsconfiguration)" : CloudWatchLogsConfiguration,
  "[LogSchemaVersion](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-logschemaversion)" : Integer,
  "[S3Configuration](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-s3configuration)" : S3Configuration
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-experimenttemplatelogconfiguration-syntax.yaml"></a>

```
  [CloudWatchLogsConfiguration](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-cloudwatchlogsconfiguration): 
    CloudWatchLogsConfiguration
  [LogSchemaVersion](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-logschemaversion): Integer
  [S3Configuration](#cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-s3configuration): 
    S3Configuration
```

## Properties<a name="aws-properties-fis-experimenttemplate-experimenttemplatelogconfiguration-properties"></a>

`CloudWatchLogsConfiguration`  <a name="cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-cloudwatchlogsconfiguration"></a>
The configuration for experiment logging to Amazon CloudWatch Logs\. The supported field is `LogGroupArn`\. For example:  
`{"LogGroupArn": "aws:arn:logs:region_name:account_id:log-group:log_group_name"}`  
*Required*: No  
*Type*: [CloudWatchLogsConfiguration](aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogSchemaVersion`  <a name="cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-logschemaversion"></a>
The schema version\. The supported value is 1\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-fis-experimenttemplate-experimenttemplatelogconfiguration-s3configuration"></a>
The configuration for experiment logging to Amazon S3\. The following fields are supported:  
+ `bucketName` \- The name of the destination bucket\.
+ `prefix` \- An optional bucket prefix\.
For example:  
`{"BucketName": "my-s3-bucket", "Prefix": "log-folder"}`  
*Required*: No  
*Type*: [S3Configuration](aws-properties-fis-experimenttemplate-s3configuration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)