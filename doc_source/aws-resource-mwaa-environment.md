# AWS::MWAA::Environment<a name="aws-resource-mwaa-environment"></a>

The `AWS::MWAA::Environment` resource creates an Amazon Managed Workflows for Apache Airflow \(MWAA\) environment\. 

## Syntax<a name="aws-resource-mwaa-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mwaa-environment-syntax.json"></a>

```
{
  "Type" : "AWS::MWAA::Environment",
  "Properties" : {
      "[AirflowConfigurationOptions](#cfn-mwaa-environment-airflowconfigurationoptions)" : Json,
      "[AirflowVersion](#cfn-mwaa-environment-airflowversion)" : String,
      "[DagS3Path](#cfn-mwaa-environment-dags3path)" : String,
      "[EnvironmentClass](#cfn-mwaa-environment-environmentclass)" : String,
      "[ExecutionRoleArn](#cfn-mwaa-environment-executionrolearn)" : String,
      "[KmsKey](#cfn-mwaa-environment-kmskey)" : String,
      "[LoggingConfiguration](#cfn-mwaa-environment-loggingconfiguration)" : LoggingConfiguration,
      "[MaxWorkers](#cfn-mwaa-environment-maxworkers)" : Integer,
      "[MinWorkers](#cfn-mwaa-environment-minworkers)" : Integer,
      "[Name](#cfn-mwaa-environment-name)" : String,
      "[NetworkConfiguration](#cfn-mwaa-environment-networkconfiguration)" : NetworkConfiguration,
      "[PluginsS3ObjectVersion](#cfn-mwaa-environment-pluginss3objectversion)" : String,
      "[PluginsS3Path](#cfn-mwaa-environment-pluginss3path)" : String,
      "[RequirementsS3ObjectVersion](#cfn-mwaa-environment-requirementss3objectversion)" : String,
      "[RequirementsS3Path](#cfn-mwaa-environment-requirementss3path)" : String,
      "[Schedulers](#cfn-mwaa-environment-schedulers)" : Integer,
      "[SourceBucketArn](#cfn-mwaa-environment-sourcebucketarn)" : String,
      "[Tags](#cfn-mwaa-environment-tags)" : Json,
      "[WebserverAccessMode](#cfn-mwaa-environment-webserveraccessmode)" : String,
      "[WeeklyMaintenanceWindowStart](#cfn-mwaa-environment-weeklymaintenancewindowstart)" : String
    }
}
```

### YAML<a name="aws-resource-mwaa-environment-syntax.yaml"></a>

```
Type: AWS::MWAA::Environment
Properties: 
  [AirflowConfigurationOptions](#cfn-mwaa-environment-airflowconfigurationoptions): Json
  [AirflowVersion](#cfn-mwaa-environment-airflowversion): String
  [DagS3Path](#cfn-mwaa-environment-dags3path): String
  [EnvironmentClass](#cfn-mwaa-environment-environmentclass): String
  [ExecutionRoleArn](#cfn-mwaa-environment-executionrolearn): String
  [KmsKey](#cfn-mwaa-environment-kmskey): String
  [LoggingConfiguration](#cfn-mwaa-environment-loggingconfiguration): 
    LoggingConfiguration
  [MaxWorkers](#cfn-mwaa-environment-maxworkers): Integer
  [MinWorkers](#cfn-mwaa-environment-minworkers): Integer
  [Name](#cfn-mwaa-environment-name): String
  [NetworkConfiguration](#cfn-mwaa-environment-networkconfiguration): 
    NetworkConfiguration
  [PluginsS3ObjectVersion](#cfn-mwaa-environment-pluginss3objectversion): String
  [PluginsS3Path](#cfn-mwaa-environment-pluginss3path): String
  [RequirementsS3ObjectVersion](#cfn-mwaa-environment-requirementss3objectversion): String
  [RequirementsS3Path](#cfn-mwaa-environment-requirementss3path): String
  [Schedulers](#cfn-mwaa-environment-schedulers): Integer
  [SourceBucketArn](#cfn-mwaa-environment-sourcebucketarn): String
  [Tags](#cfn-mwaa-environment-tags): Json
  [WebserverAccessMode](#cfn-mwaa-environment-webserveraccessmode): String
  [WeeklyMaintenanceWindowStart](#cfn-mwaa-environment-weeklymaintenancewindowstart): String
```

## Properties<a name="aws-resource-mwaa-environment-properties"></a>

`AirflowConfigurationOptions`  <a name="cfn-mwaa-environment-airflowconfigurationoptions"></a>
A list of key\-value pairs containing the Airflow configuration options for your environment\. For example, `core.default_timezone: utc`\. To learn more, see [Apache Airflow configuration options](https://docs.aws.amazon.com/mwaa/latest/userguide/configuring-env-variables.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AirflowVersion`  <a name="cfn-mwaa-environment-airflowversion"></a>
The version of Apache Airflow to use for the environment\. If no value is specified, defaults to the latest version\. Valid values: `2.0.2`, `1.10.12`, `2.2.2`, and `2.4.3`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DagS3Path`  <a name="cfn-mwaa-environment-dags3path"></a>
The relative path to the DAGs folder on your Amazon S3 bucket\. For example, `dags`\. To learn more, see [Adding or updating DAGs](https://docs.aws.amazon.com/mwaa/latest/userguide/configuring-dag-folder.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentClass`  <a name="cfn-mwaa-environment-environmentclass"></a>
The environment class type\. Valid values: `mw1.small`, `mw1.medium`, `mw1.large`\. To learn more, see [Amazon MWAA environment class](https://docs.aws.amazon.com/mwaa/latest/userguide/environment-class.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-mwaa-environment-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the execution role in IAM that allows MWAA to access AWS resources in your environment\. For example, `arn:aws:iam::123456789:role/my-execution-role`\. To learn more, see [Amazon MWAA Execution role](https://docs.aws.amazon.com/mwaa/latest/userguide/mwaa-create-role.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKey`  <a name="cfn-mwaa-environment-kmskey"></a>
The AWS Key Management Service \(KMS\) key to encrypt and decrypt the data in your environment\. You can use an AWS KMS key managed by MWAA, or a customer\-managed KMS key \(advanced\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfiguration`  <a name="cfn-mwaa-environment-loggingconfiguration"></a>
The Apache Airflow logs being sent to CloudWatch Logs: `DagProcessingLogs`, `SchedulerLogs`, `TaskLogs`, `WebserverLogs`, `WorkerLogs`\.  
*Required*: No  
*Type*: [LoggingConfiguration](aws-properties-mwaa-environment-loggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxWorkers`  <a name="cfn-mwaa-environment-maxworkers"></a>
The maximum number of workers that you want to run in your environment\. MWAA scales the number of Apache Airflow workers up to the number you specify in the `MaxWorkers` field\. For example, `20`\. When there are no more tasks running, and no more in the queue, MWAA disposes of the extra workers leaving the one worker that is included with your environment, or the number you specify in `MinWorkers`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinWorkers`  <a name="cfn-mwaa-environment-minworkers"></a>
The minimum number of workers that you want to run in your environment\. MWAA scales the number of Apache Airflow workers up to the number you specify in the `MaxWorkers` field\. When there are no more tasks running, and no more in the queue, MWAA disposes of the extra workers leaving the worker count you specify in the `MinWorkers` field\. For example, `2`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mwaa-environment-name"></a>
The name of your Amazon MWAA environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfiguration`  <a name="cfn-mwaa-environment-networkconfiguration"></a>
The VPC networking components used to secure and enable network traffic between the AWS resources for your environment\. To learn more, see [About networking on Amazon MWAA](https://docs.aws.amazon.com/mwaa/latest/userguide/networking-about.html)\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-mwaa-environment-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PluginsS3ObjectVersion`  <a name="cfn-mwaa-environment-pluginss3objectversion"></a>
The version of the plugins\.zip file on your Amazon S3 bucket\. To learn more, see [Installing custom plugins](https://docs.aws.amazon.com/mwaa/latest/userguide/configuring-dag-import-plugins.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PluginsS3Path`  <a name="cfn-mwaa-environment-pluginss3path"></a>
The relative path to the `plugins.zip` file on your Amazon S3 bucket\. For example, `plugins.zip`\. To learn more, see [Installing custom plugins](https://docs.aws.amazon.com/mwaa/latest/userguide/configuring-dag-import-plugins.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequirementsS3ObjectVersion`  <a name="cfn-mwaa-environment-requirementss3objectversion"></a>
The version of the requirements\.txt file on your Amazon S3 bucket\. To learn more, see [Installing Python dependencies](https://docs.aws.amazon.com/mwaa/latest/userguide/working-dags-dependencies.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequirementsS3Path`  <a name="cfn-mwaa-environment-requirementss3path"></a>
The relative path to the `requirements.txt` file on your Amazon S3 bucket\. For example, `requirements.txt`\. To learn more, see [Installing Python dependencies](https://docs.aws.amazon.com/mwaa/latest/userguide/working-dags-dependencies.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedulers`  <a name="cfn-mwaa-environment-schedulers"></a>
The number of schedulers that you want to run in your environment\. Valid values:   
+ **v2** \- Accepts between 2 to 5\. Defaults to 2\.
+ **v1** \- Accepts 1\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceBucketArn`  <a name="cfn-mwaa-environment-sourcebucketarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon S3 bucket where your DAG code and supporting files are stored\. For example, `arn:aws:s3:::my-airflow-bucket-unique-name`\. To learn more, see [Create an Amazon S3 bucket for Amazon MWAA](https://docs.aws.amazon.com/mwaa/latest/userguide/mwaa-s3-bucket.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mwaa-environment-tags"></a>
The key\-value tag pairs associated to your environment\. For example, `"Environment": "Staging"`\. To learn more, see [Tagging](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebserverAccessMode`  <a name="cfn-mwaa-environment-webserveraccessmode"></a>
The Apache Airflow *Web server* access mode\. To learn more, see [Apache Airflow access modes](https://docs.aws.amazon.com/mwaa/latest/userguide/configuring-networking.html)\. Valid values: `PRIVATE_ONLY` or `PUBLIC_ONLY`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeeklyMaintenanceWindowStart`  <a name="cfn-mwaa-environment-weeklymaintenancewindowstart"></a>
The day and time of the week to start weekly maintenance updates of your environment in the following format: `DAY:HH:MM`\. For example: `TUE:03:30`\. You can specify a start time in 30 minute increments only\. Supported input includes the following:  
+ MON\|TUE\|WED\|THU\|FRI\|SAT\|SUN:\(\[01\]\\\\d\|2\[0\-3\]\):\(00\|30\)
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mwaa-environment-return-values"></a>

### Ref<a name="aws-resource-mwaa-environment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the environment details\.

### Fn::GetAtt<a name="aws-resource-mwaa-environment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mwaa-environment-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN for the Amazon MWAA environment\.

`LoggingConfiguration.DagProcessingLogs.CloudWatchLogGroupArn`  <a name="LoggingConfiguration.DagProcessingLogs.CloudWatchLogGroupArn-fn::getatt"></a>
The ARN for the CloudWatch Logs group where the Apache Airflow DAG processing logs are published\.

`LoggingConfiguration.SchedulerLogs.CloudWatchLogGroupArn`  <a name="LoggingConfiguration.SchedulerLogs.CloudWatchLogGroupArn-fn::getatt"></a>
The ARN for the CloudWatch Logs group where the Apache Airflow Scheduler logs are published\.

`LoggingConfiguration.TaskLogs.CloudWatchLogGroupArn`  <a name="LoggingConfiguration.TaskLogs.CloudWatchLogGroupArn-fn::getatt"></a>
The ARN for the CloudWatch Logs group where the Apache Airflow task logs are published\.

`LoggingConfiguration.WebserverLogs.CloudWatchLogGroupArn`  <a name="LoggingConfiguration.WebserverLogs.CloudWatchLogGroupArn-fn::getatt"></a>
The ARN for the CloudWatch Logs group where the Apache Airflow Web server logs are published\.

`LoggingConfiguration.WorkerLogs.CloudWatchLogGroupArn`  <a name="LoggingConfiguration.WorkerLogs.CloudWatchLogGroupArn-fn::getatt"></a>
The ARN for the CloudWatch Logs group where the Apache Airflow Worker logs are published\.

`WebserverUrl`  <a name="WebserverUrl-fn::getatt"></a>
The URL of your Apache Airflow UI\.

## Examples<a name="aws-resource-mwaa-environment--examples"></a>



### Create a MWAA environment \- JSON<a name="aws-resource-mwaa-environment--examples--Create_a_MWAA_environment_-_JSON"></a>

The following example shows how to create a MWAA environment:

#### JSON<a name="aws-resource-mwaa-environment--examples--Create_a_MWAA_environment_-_JSON--json"></a>

```
{
    "Environment": {
        "Type": "AWS::MWAA::Environment",
        "Properties": {
            "Name": "my-airflow-environment",
            "AirflowConfigurationOptions": {
                "logging.logging_level": "INFO",
                "core.default_timezone": "utc"
            },
            "Tags": {
                "Environment": "Staging",
                "Team": "Analytics"
            },
            "NetworkConfiguration": {
                "SubnetIds": [
                    "subnet-123456",
                    "subnet-789011"
                ],
                "SecurityGroupIds": [
                    "sg-0101010"
                ]
            },
            "LoggingConfiguration": {
                "DagProcessingLogs": {
                    "Enabled": true,
                    "LogLevel": "INFO"
                },
                "SchedulerLogs": {
                    "Enabled": false,
                    "LogLevel": "INFO"
                },
                "TaskLogs": {
                    "Enabled": true,
                    "LogLevel": "INFO"
                },
                "WebserverLogs": {
                    "Enabled": false,
                    "LogLevel": "INFO"
                },
                "WorkerLogs": {
                    "Enabled": false,
                    "LogLevel": "INFO"
                }
            },
            "SourceBucketArn": "arn:aws:s3:::my-dags-bucket",
            "ExecutionRoleArn": "arn:aws:iam::012345678900:role/service-role/my-execution-role",
            "MaxWorkers": 1,
            "DagS3Path": "dags",
            "EnvironmentClass": "mw1.small"
        }
    }
}
```

### Create a MWAA environment \- YAML<a name="aws-resource-mwaa-environment--examples--Create_a_MWAA_environment_-_YAML"></a>

The following example shows how to create a MWAA environment:

#### YAML<a name="aws-resource-mwaa-environment--examples--Create_a_MWAA_environment_-_YAML--yaml"></a>

```
Environment: 
    Properties: 
      AirflowConfigurationOptions: 
        core.default_timezone: utc
        logging.logging_level: INFO
      DagS3Path: dags
      EnvironmentClass: mw1.small
      ExecutionRoleArn: "arn:aws:iam::012345678900:role/service-role/my-execution-role"
      LoggingConfiguration: 
        DagProcessingLogs: 
          Enabled: true
          LogLevel: INFO
        SchedulerLogs: 
          Enabled: false
          LogLevel: INFO
        TaskLogs: 
          Enabled: true
          LogLevel: INFO
        WebserverLogs: 
          Enabled: false
          LogLevel: INFO
        WorkerLogs: 
          Enabled: false
          LogLevel: INFO
      MaxWorkers: 1
      Name: my-airflow-environment
      NetworkConfiguration: 
        SecurityGroupIds: 
          - sg-0101010
        SubnetIds: 
          - subnet-123456
          - subnet-789011
      SourceBucketArn: "arn:aws:s3:::my-dags-bucket"
      Tags: 
        Environment: Staging
        Team: Analytics
    Type: "AWS::MWAA::Environment"
```