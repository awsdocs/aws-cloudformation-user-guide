# Amazon Elastic Container Service TaskDefinition LogConfiguration<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration"></a>

`LogConfiguration` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that configures a custom log driver for an Amazon Elastic Container Service \(Amazon ECS\) container\.

## Syntax<a name="w3ab2c21c14d886b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-syntax.json"></a>

```
{
  "[LogDriver](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver)" : String,
  "[Options](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration-syntax.yaml"></a>

```
[LogDriver](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver): String
[Options](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options):
  String: String
```

## Properties<a name="w3ab2c21c14d886b7"></a>

`LogDriver`  <a name="cfn-ecs-taskdefinition-containerdefinition-logconfiguration-logdriver"></a>
The log driver to use for the container\. This parameter requires that your container instance uses Docker Remote API Version 1\.18 or greater\. For more information, see the `logDriver` content for the [LogConfiguration](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_LogConfiguration.html) data type in the *Amazon Elastic Container Service API Reference*\.  
*Required*: Yes  
*Type*: String

`Options`  <a name="cfn-ecs-taskdefinition-containerdefinition-logconfiguration-options"></a>
The configuration options to send to the log driver\. This parameter requires that your container instance uses Docker Remote API Version 1\.18 or greater\.   
*Required*: No  
*Type*: Key\-value pairs, with the option name as the key and the option value as the value\.