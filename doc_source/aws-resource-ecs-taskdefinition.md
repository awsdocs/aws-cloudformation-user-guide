# AWS::ECS::TaskDefinition<a name="aws-resource-ecs-taskdefinition"></a>

The `AWS::ECS::TaskDefinition` resource describes the container and volume definitions of an Amazon Elastic Container Service \(Amazon ECS\) task\. You can specify which Docker images to use, the required resources, and other configurations related to launching the task definition through an Amazon ECS service or task\.

**Topics**
+ [Syntax](#aws-resource-ecs-taskdefinition-syntax)
+ [Properties](#aws-resource-ecs-taskdefinition-properties)
+ [Return Value](#aws-resource-ecs-taskdefinition-returnvalues)
+ [Examples](#aws-resource-ecs-taskdefinition-examples)
+ [See Also](#aws-resource-ecs-taskdefinition-seealso)

## Syntax<a name="aws-resource-ecs-taskdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-taskdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::TaskDefinition",
  "Properties" : {
    "[Volumes](#cfn-ecs-taskdefinition-volumes)" : [ Volume Definition, ... ],
    "[Cpu](#cfn-ecs-taskdefinition-cpu)" : String,
    "[ExecutionRoleArn](#cfn-ecs-taskdefinition-executionrolearn)" : String,
    "[Family](#cfn-ecs-taskdefinition-family)" : String,
    "[Memory](#cfn-ecs-taskdefinition-memory)" : String,
    "[NetworkMode](#cfn-ecs-taskdefinition-networkmode)" : String,
    "[PlacementConstraints](#cfn-ecs-taskdefinition-placementconstraints)" : TaskDefinitionPlacementConstraint,
    "[RequiresCompatibilities](#cfn-ecs-taskdefinition-requirescompatibilities)" : [ String, ... ],
    "[TaskRoleArn](#cfn-ecs-taskdefinition-taskrolearn)" : String,
    "[ContainerDefinitions](#cfn-ecs-taskdefinition-containerdefinition)" : [ Container Definition, ... ]
  }
}
```

### YAML<a name="aws-resource-ecs-taskdefinition-syntax.yaml"></a>

```
Type: "AWS::ECS::TaskDefinition"
Properties: 
  [Volumes](#cfn-ecs-taskdefinition-volumes):
    - Volume Definition
  [Cpu](#cfn-ecs-taskdefinition-cpu): String
  [ExecutionRoleArn](#cfn-ecs-taskdefinition-executionrolearn): String
  [Family](#cfn-ecs-taskdefinition-family): String
  [Memory](#cfn-ecs-taskdefinition-memory): String
  [NetworkMode](#cfn-ecs-taskdefinition-networkmode): String
  [PlacementConstraints](#cfn-ecs-taskdefinition-placementconstraints):
    - TaskDefinitionPlacementConstraint
  [RequiresCompatibilities](#cfn-ecs-taskdefinition-requirescompatibilities):
    - String
  [TaskRoleArn](#cfn-ecs-taskdefinition-taskrolearn): String
  [ContainerDefinitions](#cfn-ecs-taskdefinition-containerdefinition):
    - Container Definition
```

## Properties<a name="aws-resource-ecs-taskdefinition-properties"></a>

For more information on properties and valid parameters, see [RegisterTaskDefinition](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RegisterTaskDefinition.html) in the *Amazon Elastic Container Service API Reference*\.

`ContainerDefinitions`  <a name="cfn-ecs-taskdefinition-containerdefinition"></a>
A list of container definitions in JSON format that describes the containers that make up your task\.  
*Required*: Yes  
*Type*: List of [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Cpu`  <a name="cfn-ecs-taskdefinition-cpu"></a>
The number of `cpu` units used by the task\. If using the EC2 launch type, this field is optional and any value can be used\. If you are using the Fargate launch type, this field is required and you must use one of the following values, which determines your range of valid values for the `memory` parameter:  
+ 256 \(\.25 vCPU\) \- Available `memory` values: 0\.5GB, 1GB, 2GB
+ 512 \(\.5 vCPU\) \- Available `memory` values: 1GB, 2GB, 3GB, 4GB
+ 1024 \(1 vCPU\) \- Available `memory` values: 2GB, 3GB, 4GB, 5GB, 6GB, 7GB, 8GB
+ 2048 \(2 vCPU\) \- Available `memory` values: Between 4GB and 16GB in 1GB increments
+ 4096 \(4 vCPU\) \- Available `memory` values: Between 8GB and 30GB in 1GB increments
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ExecutionRoleArn`  <a name="cfn-ecs-taskdefinition-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the task execution role that containers in this task can assume\. All containers in this task are granted the permissions that are specified in this role\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Family`  <a name="cfn-ecs-taskdefinition-family"></a>
The name of a family that this task definition is registered to\. A *family* groups multiple versions of a task definition\. Amazon ECS gives the first task definition that you registered to a family a revision number of 1\. Amazon ECS gives sequential revision numbers to each task definition that you add\.  
To use revision numbers when you update a task definition, specify this property\. If you don't specify a value, AWS CloudFormation generates a new task definition each time that you update it\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Memory`  <a name="cfn-ecs-taskdefinition-memory"></a>
The amount \(in MiB\) of memory used by the task\. If using the EC2 launch type, this field is optional and any value can be used\. If you are using the Fargate launch type, this field is required and you must use one of the following values, which determines your range of valid values for the `cpu` parameter:  
+ 0\.5GB, 1GB, 2GB \- Available `cpu` values: 256 \(\.25 vCPU\)
+ 1GB, 2GB, 3GB, 4GB \- Available `cpu` values: 512 \(\.5 vCPU\)
+ 2GB, 3GB, 4GB, 5GB, 6GB, 7GB, 8GB \- Available `cpu` values: 1024 \(1 vCPU\)
+ Between 4GB and 16GB in 1GB increments \- Available `cpu` values: 2048 \(2 vCPU\)
+ Between 8GB and 30GB in 1GB increments \- Available `cpu` values: 4096 \(4 vCPU\)
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NetworkMode`  <a name="cfn-ecs-taskdefinition-networkmode"></a>
The Docker networking mode to use for the containers in the task, such as `none`, `bridge`, or `host`\. For information about network modes, see [http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RegisterTaskDefinition.html](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RegisterTaskDefinition.html) in the [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) topic in the *Amazon Elastic Container Service Developer Guide*\.  
For Fargate launch types, you can specify `awsvpc` only\. The `none`, `bridge`, or `host` option won't work for Fargate launch types\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PlacementConstraints`  <a name="cfn-ecs-taskdefinition-placementconstraints"></a>
The placement constraints for the tasks in the service\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service Service PlacementConstraint](aws-properties-ecs-taskdefinition-placementconstraints-taskdefinitionplacementconstraint.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RequiresCompatibilities`  <a name="cfn-ecs-taskdefinition-requirescompatibilities"></a>
The launch type the task requires\. If no value is specified, it will default to `EC2`\. Valid values include `EC2` and `FARGATE`\.  
*Required*: No  
*Type*: List of Strings  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TaskRoleArn`  <a name="cfn-ecs-taskdefinition-taskrolearn"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that grants containers in the task permission to call AWS APIs on your behalf\. For more information, see [IAM Roles for Tasks](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Volumes`  <a name="cfn-ecs-taskdefinition-volumes"></a>
A list of volume definitions in JSON format for the volumes that you can use in your container definitions\.  
*Required*: No  
*Type*: List of [Amazon Elastic Container Service TaskDefinition Volumes](aws-properties-ecs-taskdefinition-volumes.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-ecs-taskdefinition-returnvalues"></a>

### Ref<a name="aws-resource-ecs-taskdefinition-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the Amazon Resource Name \(ARN\)\.

In the following example, the `Ref` function returns the ARN of the `MyTaskDefinition` task, such as `arn:aws:ecs:us-west-2:123456789012:task/1abf0f6d-a411-4033-b8eb-a4eed3ad252a`\.

```
{ "Ref": "MyTaskDefinition" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-ecs-taskdefinition-examples"></a>

### <a name="aws-resource-ecs-taskdefinition-example1"></a>

The following example defines an Amazon ECS task definition, which includes two container definitions and one volume definition\.

#### JSON<a name="aws-resource-ecs-taskdefinition-example.json"></a>

```
"taskdefinition": {
  "Type": "AWS::ECS::TaskDefinition",
  "Properties" : {
    "ContainerDefinitions" : [
    {
      "Name": {"Ref": "AppName"},
      "MountPoints": [
        {
          "SourceVolume": "my-vol",
          "ContainerPath": "/var/www/my-vol"
        }
      ],
      "Image":"amazon/amazon-ecs-sample",
      "Cpu": "10",
      "PortMappings":[
        {
          "ContainerPort": {"Ref":"AppContainerPort"},
          "HostPort": {"Ref":"AppHostPort"}
        }
      ],
      "EntryPoint": [
        "/usr/sbin/apache2",
        "-D",
        "FOREGROUND"
      ],
      "Memory":"500",
      "Essential": "true"
    },
    {
      "Name": "busybox",
      "Image": "busybox",
      "Cpu": "10",
      "EntryPoint": [
        "sh",
        "-c"
      ],
      "Memory": "500",
      "Command": [
        "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
      ],
      "Essential" : "false",
      "VolumesFrom": [
        {
          "SourceContainer": {"Ref":"AppName"}
        }
      ]
    }],
    "Volumes": [
    {
      "Host": {
        "SourcePath": "/var/lib/docker/vfs/dir/"
      },
      "Name": "my-vol"
    }]
  }
}
```

#### YAML<a name="aws-resource-ecs-taskdefinition-example.yaml"></a>

```
taskdefinition: 
  Type: "AWS::ECS::TaskDefinition"
  Properties: 
    ContainerDefinitions: 
      - 
        Name: 
          Ref: "AppName"
        MountPoints: 
          - 
            SourceVolume: "my-vol"
            ContainerPath: "/var/www/my-vol"
        Image: "amazon/amazon-ecs-sample"
        Cpu: "10"
        PortMappings: 
          - 
            ContainerPort: 
              Ref: "AppContainerPort"
            HostPort: 
              Ref: "AppHostPort"
        EntryPoint: 
          - "/usr/sbin/apache2"
          - "-D"
          - "FOREGROUND"
        Memory: "500"
        Essential: "true"
      - 
        Name: "busybox"
        Image: "busybox"
        Cpu: "10"
        EntryPoint: 
          - "sh"
          - "-c"
        Memory: "500"
        Command: 
          - "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
        Essential: "false"
        VolumesFrom: 
          - 
            SourceContainer: 
              Ref: "AppName"
    Volumes: 
      - 
        Host: 
          SourcePath: "/var/lib/docker/vfs/dir/"
        Name: "my-vol"
```

### <a name="aws-resource-ecs-taskdefinition-example2"></a>

The following example defines an Amazon ECS task definition that specifies `EC2` and `FARGATE` as required compatibilities\.

#### JSON<a name="aws-resource-ecs-taskdefinition-example2.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "taskdefinition": {
      "Type": "AWS::ECS::TaskDefinition",
      "Properties": {
        "RequiresCompatibilities": [
          "EC2",
          "FARGATE"
        ],
        "ContainerDefinitions": [
          {
            "Name": "my-app",
            "MountPoints": [
              {
                "SourceVolume": "my-vol",
                "ContainerPath": "/var/www/my-vol"
              }
            ],
            "Image": "amazon/amazon-ecs-sample",
            "Cpu": "10",
            "EntryPoint": [
              "/usr/sbin/apache2",
              "-D",
              "FOREGROUND"
            ],
            "Memory": "500",
            "Essential": "true"
          },
          {
            "Name": "busybox",
            "Image": "busybox",
            "Cpu": "10",
            "EntryPoint": [
              "sh",
              "-c"
            ],
            "Memory": "500",
            "Command": [
              "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
            ],
            "Essential": "false",
            "VolumesFrom": [
              {
                "SourceContainer": "my-app"
              }
            ]
          }
        ],
        "Volumes": [
          {
            "Host": {
              "SourcePath": "/var/lib/docker/vfs/dir/"
            },
            "Name": "my-vol"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ecs-taskdefinition-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  taskdefinition: 
    Type: "AWS::ECS::TaskDefinition"
    Properties: 
      RequiresCompatibilities:
        - "EC2"
        - "FARGATE"
      ContainerDefinitions: 
        - 
          Name: "my-app"
          MountPoints: 
            - 
              SourceVolume: "my-vol"
              ContainerPath: "/var/www/my-vol"
          Image: "amazon/amazon-ecs-sample"
          Cpu: "10"
          EntryPoint: 
            - "/usr/sbin/apache2"
            - "-D"
            - "FOREGROUND"
          Memory: "500"
          Essential: "true"
        - 
          Name: "busybox"
          Image: "busybox"
          Cpu: "10"
          EntryPoint: 
            - "sh"
            - "-c"
          Memory: "500"
          Command: 
            - "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
          Essential: "false"
          VolumesFrom: 
            - 
              SourceContainer: "my-app"
      Volumes: 
        - 
          Host: 
            SourcePath: "/var/lib/docker/vfs/dir/"
          Name: "my-vol"
```

## See Also<a name="aws-resource-ecs-taskdefinition-seealso"></a>

For a complete sample template that shows how you can create an Amazon ECS cluster and service, see [Amazon Elastic Container Service Template Snippets](quickref-ecs.md)\.