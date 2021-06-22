# AWS::MWAA::Environment<a name="aws-resource-mwaa-environment"></a>

The `AWS::MWAA::Environment` resource creates an Amazon Managed Workflows for Apache Airflow \(MWAA\) environment\. 

**Topics**
+ [Syntax](#aws-resource-mwaa-environment-syntax)
+ [Properties](#aws-resource-mwaa-environment-properties)
+ [Return values](#aws-resource-mwaa-environment-return-values)
+ [Examples](#aws-resource-mwaa-environment--examples)
+ [AWS::MWAA::Environment LoggingConfiguration](aws-properties-mwaa-environment-loggingconfiguration.md)
+ [AWS::MWAA::Environment ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)
+ [AWS::MWAA::Environment NetworkConfiguration](aws-properties-mwaa-environment-networkconfiguration.md)
+ [AWS::MWAA::Environment TagMap](aws-properties-mwaa-environment-tagmap.md)

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
      "[Tags](#cfn-mwaa-environment-tags)" : TagMap,
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
  [Tags](#cfn-mwaa-environment-tags): 
    TagMap
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
The version of Apache Airflow to use for the environment\. For example: `1.10.12`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DagS3Path`  <a name="cfn-mwaa-environment-dags3path"></a>
The relative path to the DAGs folder in your Amazon S3 bucket\. For example: `dags`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentClass`  <a name="cfn-mwaa-environment-environmentclass"></a>
The environment class name\. An environment class determines the size of your metadata database and containers\. Valid values: `mw1.small`, `mw1.medium`, or `mw1.large`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-mwaa-environment-executionrolearn"></a>
The ARN of the execution role in IAM that allows MWAA to access AWS resources in your environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKey`  <a name="cfn-mwaa-environment-kmskey"></a>
The AWS Key Management Service \(KMS\) key to encrypt and decrypt the data in your environment\. You can use an AWS KMS key managed by MWAA, or a custom KMS key \(advanced\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfiguration`  <a name="cfn-mwaa-environment-loggingconfiguration"></a>
The Apache Airflow logging settings for the environment\.  
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
The name of your MWAA environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfiguration`  <a name="cfn-mwaa-environment-networkconfiguration"></a>
The VPC networking components for your Amazon MWAA environment\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-mwaa-environment-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PluginsS3ObjectVersion`  <a name="cfn-mwaa-environment-pluginss3objectversion"></a>
The version of your plugins\.zip file\. To learn more, see [How S3 Versioning works](https://docs.aws.amazon.com/AmazonS3/latest/userguide/versioning-workflows.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PluginsS3Path`  <a name="cfn-mwaa-environment-pluginss3path"></a>
The relative path of the plugins\.zip file in your Amazon S3 bucket\. For example, if the file is at the root of your Amazon S3 bucket, specify `plugins.zip`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequirementsS3ObjectVersion`  <a name="cfn-mwaa-environment-requirementss3objectversion"></a>
The version of the requirements\.txt file\. To learn more, see [How S3 Versioning works](https://docs.aws.amazon.com/AmazonS3/latest/userguide/versioning-workflows.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequirementsS3Path`  <a name="cfn-mwaa-environment-requirementss3path"></a>
The relative path of the requirements\.txt file in your Amazon S3 bucket\. For example, if the file is at the root of your Amazon S3 bucket, specify `requirements.txt`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedulers`  <a name="cfn-mwaa-environment-schedulers"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceBucketArn`  <a name="cfn-mwaa-environment-sourcebucketarn"></a>
The ARN of the Amazon S3 bucket where your DAG code and supporting files are stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mwaa-environment-tags"></a>
A list of key\-value pairs for tags you want to attach to your environment\.  
*Required*: No  
*Type*: [TagMap](aws-properties-mwaa-environment-tagmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebserverAccessMode`  <a name="cfn-mwaa-environment-webserveraccessmode"></a>
The mode to access the Apache Airflow web server\. A public network allows users to access the Apache Airflow UI over the Internet using their IAM credentials\. A private network limits access to Apache Airflow to users within a VPC\. Valid values: `PRIVATE_ONLY` or `PUBLIC_ONLY`\.  
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