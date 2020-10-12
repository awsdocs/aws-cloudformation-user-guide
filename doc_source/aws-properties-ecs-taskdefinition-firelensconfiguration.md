# AWS::ECS::TaskDefinition FirelensConfiguration<a name="aws-properties-ecs-taskdefinition-firelensconfiguration"></a>

The FireLens configuration for the container\. This is used to specify and configure a log router for container logs\. For more information, see [Custom Log Routing](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_firelens.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-taskdefinition-firelensconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-firelensconfiguration-syntax.json"></a>

```
{
  "[Options](#cfn-ecs-taskdefinition-firelensconfiguration-options)" : {Key : Value, ...},
  "[Type](#cfn-ecs-taskdefinition-firelensconfiguration-type)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-firelensconfiguration-syntax.yaml"></a>

```
  [Options](#cfn-ecs-taskdefinition-firelensconfiguration-options): 
    Key : Value
  [Type](#cfn-ecs-taskdefinition-firelensconfiguration-type): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-firelensconfiguration-properties"></a>

`Options`  <a name="cfn-ecs-taskdefinition-firelensconfiguration-options"></a>
The options to use when configuring the log router\. This field is optional and can be used to add additional metadata, such as the task, task definition, cluster, and container instance details to the log event\.  
 If specified, valid option keys are:  
+ `enable-ecs-log-metadata`, which can be `true` or `false`
+ `config-file-type`, which can be `s3` or `file`
+ `config-file-value`, which is either an S3 ARN or a file path
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ecs-taskdefinition-firelensconfiguration-type"></a>
The log router to use\. The valid values are `fluentd` or `fluentbit`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `fluentbit | fluentd`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)