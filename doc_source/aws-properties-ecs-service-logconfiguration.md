# AWS::ECS::Service LogConfiguration<a name="aws-properties-ecs-service-logconfiguration"></a>

The log configuration for the container\. This parameter maps to `LogConfig` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--log-driver` option to [https://docs.docker.com/engine/reference/commandline/run/](https://docs.docker.com/engine/reference/commandline/run/)\.

By default, containers use the same logging driver that the Docker daemon uses\. However, the container might use a different logging driver than the Docker daemon by specifying a log driver configuration in the container definition\. For more information about the options for different supported log drivers, see [Configure logging drivers](https://docs.docker.com/engine/admin/logging/overview/) in the Docker documentation\.

Understand the following when specifying a log configuration for your containers\.
+ Amazon ECS currently supports a subset of the logging drivers available to the Docker daemon \(shown in the valid values below\)\. Additional log drivers may be available in future releases of the Amazon ECS container agent\.
+ This parameter requires version 1\.18 of the Docker Remote API or greater on your container instance\.
+ For tasks that are hosted on Amazon EC2 instances, the Amazon ECS container agent must register the available logging drivers with the `ECS_AVAILABLE_LOGGING_DRIVERS` environment variable before containers placed on that instance can use these log configuration options\. For more information, see [Amazon ECS container agent configuration](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-agent-config.html) in the *Amazon Elastic Container Service Developer Guide*\.
+ For tasks that are on AWS Fargate, because you don't have access to the underlying infrastructure your tasks are hosted on, any additional software needed must be installed outside of the task\. For example, the Fluentd output aggregators or a remote host running Logstash to send Gelf logs to\.

## Syntax<a name="aws-properties-ecs-service-logconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-logconfiguration-syntax.json"></a>

```
{
  "[LogDriver](#cfn-ecs-service-logconfiguration-logdriver)" : String,
  "[Options](#cfn-ecs-service-logconfiguration-options)" : {Key : Value, ...},
  "[SecretOptions](#cfn-ecs-service-logconfiguration-secretoptions)" : [ Secret, ... ]
}
```

### YAML<a name="aws-properties-ecs-service-logconfiguration-syntax.yaml"></a>

```
  [LogDriver](#cfn-ecs-service-logconfiguration-logdriver): String
  [Options](#cfn-ecs-service-logconfiguration-options): 
    Key : Value
  [SecretOptions](#cfn-ecs-service-logconfiguration-secretoptions): 
    - Secret
```

## Properties<a name="aws-properties-ecs-service-logconfiguration-properties"></a>

`LogDriver`  <a name="cfn-ecs-service-logconfiguration-logdriver"></a>
The log driver to use for the container\.  
For tasks on AWS Fargate, the supported log drivers are `awslogs`, `splunk`, and `awsfirelens`\.  
For tasks hosted on Amazon EC2 instances, the supported log drivers are `awslogs`, `fluentd`, `gelf`, `json-file`, `journald`, `logentries`,`syslog`, `splunk`, and `awsfirelens`\.  
For more information about using the `awslogs` log driver, see [Using the awslogs log driver](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html) in the *Amazon Elastic Container Service Developer Guide*\.  
For more information about using the `awsfirelens` log driver, see [Custom log routing](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_firelens.html) in the *Amazon Elastic Container Service Developer Guide*\.  
If you have a custom driver that isn't listed, you can fork the Amazon ECS container agent project that's [available on GitHub](https://github.com/aws/amazon-ecs-agent) and customize it to work with that driver\. We encourage you to submit pull requests for changes that you would like to have included\. However, we don't currently provide support for running modified copies of this software\.
*Required*: No  
*Type*: String  
*Allowed values*: `awsfirelens | awslogs | fluentd | gelf | journald | json-file | splunk | syslog`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-ecs-service-logconfiguration-options"></a>
The configuration options to send to the log driver\. This parameter requires version 1\.19 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log in to your container instance and run the following command: `sudo docker version --format '{{.Server.APIVersion}}'`   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretOptions`  <a name="cfn-ecs-service-logconfiguration-secretoptions"></a>
The secrets to pass to the log configuration\. For more information, see [Specifying sensitive data](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/specifying-sensitive-data.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: List of [Secret](aws-properties-ecs-service-secret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)