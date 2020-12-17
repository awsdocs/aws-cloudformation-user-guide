# AWS::Batch::JobDefinition LogConfiguration<a name="aws-properties-batch-jobdefinition-containerproperties-logconfiguration"></a>

Log configuration options to send to a custom log driver for the container\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-logconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-logconfiguration-syntax.json"></a>

```
{
  "[LogDriver](#cfn-batch-jobdefinition-containerproperties-logconfiguration-logdriver)" : String,
  "[Options](#cfn-batch-jobdefinition-containerproperties-logconfiguration-options)" : Json,
  "[SecretOptions](#cfn-batch-jobdefinition-containerproperties-logconfiguration-secretoptions)" : [ Secret, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-logconfiguration-syntax.yaml"></a>

```
  [LogDriver](#cfn-batch-jobdefinition-containerproperties-logconfiguration-logdriver): String
  [Options](#cfn-batch-jobdefinition-containerproperties-logconfiguration-options): Json
  [SecretOptions](#cfn-batch-jobdefinition-containerproperties-logconfiguration-secretoptions): 
    - Secret
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-logconfiguration-properties"></a>

`LogDriver`  <a name="cfn-batch-jobdefinition-containerproperties-logconfiguration-logdriver"></a>
The log driver to use for the container\. The valid values listed for this parameter are log drivers that the Amazon ECS container agent can communicate with by default\.  
The supported log drivers are `awslogs`, `fluentd`, `gelf`, `json-file`, `journald`, `logentries`, `syslog`, and `splunk`\.  
Jobs running on Fargate resources are restricted to the `awslogs` and `splunk` log drivers\.  
awslogs  
Specifies the Amazon CloudWatch Logs logging driver\. For more information, see [Using the awslogs Log Driver](https://docs.aws.amazon.com/batch/latest/userguide/using_awslogs.html) in the *AWS Batch User Guide* and [Amazon CloudWatch Logs logging driver](https://docs.docker.com/config/containers/logging/awslogs/) in the Docker documentation\.  
fluentd  
Specifies the Fluentd logging driver\. For more information, including usage and options, see [Fluentd logging driver](https://docs.docker.com/config/containers/logging/fluentd/) in the Docker documentation\.  
gelf  
Specifies the Graylog Extended Format \(GELF\) logging driver\. For more information, including usage and options, see [Graylog Extended Format logging driver](https://docs.docker.com/config/containers/logging/gelf/) in the Docker documentation\.  
journald  
Specifies the journald logging driver\. For more information, including usage and options, see [Journald logging driver](https://docs.docker.com/config/containers/logging/journald/) in the Docker documentation\.  
json\-file  
Specifies the JSON file logging driver\. For more information, including usage and options, see [JSON File logging driver](https://docs.docker.com/config/containers/logging/json-file/) in the Docker documentation\.  
splunk  
Specifies the Splunk logging driver\. For more information, including usage and options, see [Splunk logging driver](https://docs.docker.com/config/containers/logging/splunk/) in the Docker documentation\.  
syslog  
Specifies the syslog logging driver\. For more information, including usage and options, see [Syslog logging driver](https://docs.docker.com/config/containers/logging/syslog/) in the Docker documentation\.
If you have a custom driver that'sn't listed earlier that you want to work with the Amazon ECS container agent, you can fork the Amazon ECS container agent project that's [available on GitHub](https://github.com/aws/amazon-ecs-agent) and customize it to work with that driver\. We encourage you to submit pull requests for changes that you want to have included\. However, Amazon Web Services doesn't currently support running modified copies of this software\.
This parameter requires version 1\.18 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log into your container instance and run the following command: `sudo docker version | grep "Server API version"`   
*Required*: Yes  
*Type*: String  
*Allowed values*: `awslogs | fluentd | gelf | journald | json-file | splunk | syslog`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-batch-jobdefinition-containerproperties-logconfiguration-options"></a>
The configuration options to send to the log driver\. This parameter requires version 1\.19 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log into your container instance and run the following command: `sudo docker version | grep "Server API version"`   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretOptions`  <a name="cfn-batch-jobdefinition-containerproperties-logconfiguration-secretoptions"></a>
The secrets to pass to the log configuration\. For more information, see [Specifying Sensitive Data](https://docs.aws.amazon.com/batch/latest/userguide/specifying-sensitive-data.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: List of [Secret](aws-properties-batch-jobdefinition-secret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)