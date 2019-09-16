# AWS::ECS::TaskDefinition LogConfiguration<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration"></a>

The `LogConfiguration` property specifies log configuration options to send to a custom log driver for the container\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-syntax.json"></a>

```
{
  "[LogDriver](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver)" : String,
  "[Options](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options)" : {Key : Value, ...},
  "[SecretOptions](#cfn-ecs-taskdefinition-logconfiguration-secretoptions)" : [ [Secret](aws-properties-ecs-taskdefinition-secret.md), ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-syntax.yaml"></a>

```
  [LogDriver](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver): String
  [Options](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options): 
    Key : Value
  [SecretOptions](#cfn-ecs-taskdefinition-logconfiguration-secretoptions): 
    - [Secret](aws-properties-ecs-taskdefinition-secret.md)
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-properties"></a>

`LogDriver`  <a name="cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver"></a>
The log driver to use for the container\. The valid values listed for this parameter are log drivers that the Amazon ECS container agent can communicate with by default\.  
For tasks using the Fargate launch type, the supported log drivers are `awslogs` and `splunk`\.  
For tasks using the EC2 launch type, the supported log drivers are `awslogs`, `fluentd`, `gelf`, `json-file`, `journald`, `logentries`, `syslog`, and `splunk`\.  
For more information about using the `awslogs` log driver, see [Using the awslogs Log Driver](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html) in the *Amazon Elastic Container Service Developer Guide*\.  
If you have a custom driver that is not listed above that you would like to work with the Amazon ECS container agent, you can fork the Amazon ECS container agent project that is [available on GitHub](https://github.com/aws/amazon-ecs-agent) and customize it to work with that driver\. We encourage you to submit pull requests for changes that you would like to have included\. However, Amazon Web Services does not currently support running modified copies of this software\.
This parameter requires version 1\.18 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log in to your container instance and run the following command: `sudo docker version --format '{{.Server.APIVersion}}'`   
*Required*: Yes  
*Type*: String  
*Allowed Values*: `awsfirelens | awslogs | fluentd | gelf | journald | json-file | splunk | syslog`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Options`  <a name="cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options"></a>
The configuration options to send to the log driver\. This parameter requires version 1\.19 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log in to your container instance and run the following command: `sudo docker version --format '{{.Server.APIVersion}}'`   
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretOptions`  <a name="cfn-ecs-taskdefinition-logconfiguration-secretoptions"></a>
The secrets to pass to the log configuration\.  
*Required*: No  
*Type*: List of [Secret](aws-properties-ecs-taskdefinition-secret.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)