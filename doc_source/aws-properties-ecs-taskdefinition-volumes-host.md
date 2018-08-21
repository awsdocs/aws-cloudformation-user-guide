# Amazon Elastic Container Service TaskDefinition Volumes Host<a name="aws-properties-ecs-taskdefinition-volumes-host"></a>

`Host` is a property of the [Amazon Elastic Container Service TaskDefinition Volumes](aws-properties-ecs-taskdefinition-volumes.md) property that specifies the data volume path on the host container instance\.

## Syntax<a name="w3ab2c21c14d914b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-volumes-host-syntax.json"></a>

```
{
  "[SourcePath](#cfn-ecs-taskdefinition-volumes-host-sourcepath)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-volumes-host-syntax.yaml"></a>

```
[SourcePath](#cfn-ecs-taskdefinition-volumes-host-sourcepath): String
```

## Properties<a name="w3ab2c21c14d914b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`SourcePath`  <a name="cfn-ecs-taskdefinition-volumes-host-sourcepath"></a>
The data volume path on the host container instance\.  
If you don't specify this parameter, the Docker daemon assigns a path for you, but the data volume might not persist after the associated container stops running\. If you do specify a path, the data volume persists at that location on the host container instance until you manually delete it\.  
*Required*: No  
*Type*: String