# AWS::ECS::TaskDefinition<a name="aws-resource-ecs-taskdefinition"></a>

The `AWS::ECS::TaskDefinition` resource describes the container and volume definitions of an Amazon Elastic Container Service \(Amazon ECS\) task\. You can specify which Docker images to use, the required resources, and other configurations related to launching the task definition through an Amazon ECS service or task\.

## Syntax<a name="aws-resource-ecs-taskdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-taskdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::TaskDefinition",
  "Properties" : {
      "[ContainerDefinitions](#cfn-ecs-taskdefinition-containerdefinitions)" : [ [ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md), ... ],
      "[Cpu](#cfn-ecs-taskdefinition-cpu)" : String,
      "[ExecutionRoleArn](#cfn-ecs-taskdefinition-executionrolearn)" : String,
      "[Family](#cfn-ecs-taskdefinition-family)" : String,
      "[Memory](#cfn-ecs-taskdefinition-memory)" : String,
      "[NetworkMode](#cfn-ecs-taskdefinition-networkmode)" : String,
      "[PlacementConstraints](#cfn-ecs-taskdefinition-placementconstraints)" : [ [TaskDefinitionPlacementConstraint](aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint.md), ... ],
      "[ProxyConfiguration](#cfn-ecs-taskdefinition-proxyconfiguration)" : [ProxyConfiguration](aws-properties-ecs-taskdefinition-proxyconfiguration.md),
      "[RequiresCompatibilities](#cfn-ecs-taskdefinition-requirescompatibilities)" : [ String, ... ],
      "[TaskRoleArn](#cfn-ecs-taskdefinition-taskrolearn)" : String,
      "[Volumes](#cfn-ecs-taskdefinition-volumes)" : [ [Volume](aws-properties-ecs-taskdefinition-volumes.md), ... ]
    }
}
```

### YAML<a name="aws-resource-ecs-taskdefinition-syntax.yaml"></a>

```
Type: AWS::ECS::TaskDefinition
Properties:
  [ContainerDefinitions](#cfn-ecs-taskdefinition-containerdefinitions):
    - [ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md)
  [Cpu](#cfn-ecs-taskdefinition-cpu): String
  [ExecutionRoleArn](#cfn-ecs-taskdefinition-executionrolearn): String
  [Family](#cfn-ecs-taskdefinition-family): String
  [Memory](#cfn-ecs-taskdefinition-memory): String
  [NetworkMode](#cfn-ecs-taskdefinition-networkmode): String
  [PlacementConstraints](#cfn-ecs-taskdefinition-placementconstraints):
    - [TaskDefinitionPlacementConstraint](aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint.md)
  [ProxyConfiguration](#cfn-ecs-taskdefinition-proxyconfiguration):
    [ProxyConfiguration](aws-properties-ecs-taskdefinition-proxyconfiguration.md)
  [RequiresCompatibilities](#cfn-ecs-taskdefinition-requirescompatibilities):
    - String
  [TaskRoleArn](#cfn-ecs-taskdefinition-taskrolearn): String
  [Volumes](#cfn-ecs-taskdefinition-volumes):
    - [Volume](aws-properties-ecs-taskdefinition-volumes.md)
```

## Properties<a name="aws-resource-ecs-taskdefinition-properties"></a>

`ContainerDefinitions`  <a name="cfn-ecs-taskdefinition-containerdefinitions"></a>
A list of container definitions in JSON format that describe the different containers that make up your task\. For more information about container definition parameters and defaults, see [Amazon ECS Task Definitions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_defintions.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No
*Type*: List of [ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md)
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Cpu`  <a name="cfn-ecs-taskdefinition-cpu"></a>
The number of `cpu` units used by the task\. If you are using the EC2 launch type, this field is optional and any value can be used\. If you are using the Fargate launch type, this field is required and you must use one of the following values, which determines your range of valid values for the `memory` parameter:
+ 256 \(\.25 vCPU\) \- Available `memory` values: 512 \(0\.5 GB\), 1024 \(1 GB\), 2048 \(2 GB\)
+ 512 \(\.5 vCPU\) \- Available `memory` values: 1024 \(1 GB\), 2048 \(2 GB\), 3072 \(3 GB\), 4096 \(4 GB\)
+ 1024 \(1 vCPU\) \- Available `memory` values: 2048 \(2 GB\), 3072 \(3 GB\), 4096 \(4 GB\), 5120 \(5 GB\), 6144 \(6 GB\), 7168 \(7 GB\), 8192 \(8 GB\)
+ 2048 \(2 vCPU\) \- Available `memory` values: Between 4096 \(4 GB\) and 16384 \(16 GB\) in increments of 1024 \(1 GB\)
+ 4096 \(4 vCPU\) \- Available `memory` values: Between 8192 \(8 GB\) and 30720 \(30 GB\) in increments of 1024 \(1 GB\)
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecutionRoleArn`  <a name="cfn-ecs-taskdefinition-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the task execution role that containers in this task can assume\. All containers in this task are granted the permissions that are specified in this role\.
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-ecs-taskdefinition-family"></a>
The name of a family that this task definition is registered to\. A family groups multiple versions of a task definition\. Amazon ECS gives the first task definition that you registered to a family a revision number of 1\. Amazon ECS gives sequential revision numbers to each task definition that you add\.
To use revision numbers when you update a task definition, specify this property\. If you don't specify a value, AWS CloudFormation generates a new task definition each time that you update it\.
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Memory`  <a name="cfn-ecs-taskdefinition-memory"></a>
The amount \(in MiB\) of memory used by the task\. If using the EC2 launch type, this field is optional and any value can be used\. If using the Fargate launch type, this field is required and you must use one of the following values, which determines your range of valid values for the `cpu` parameter:
+ 512 \(0\.5 GB\), 1024 \(1 GB\), 2048 \(2 GB\) \- Available `cpu` values: 256 \(\.25 vCPU\)
+ 1024 \(1 GB\), 2048 \(2 GB\), 3072 \(3 GB\), 4096 \(4 GB\) \- Available `cpu` values: 512 \(\.5 vCPU\)
+ 2048 \(2 GB\), 3072 \(3 GB\), 4096 \(4 GB\), 5120 \(5 GB\), 6144 \(6 GB\), 7168 \(7 GB\), 8192 \(8 GB\) \- Available `cpu` values: 1024 \(1 vCPU\)
+ Between 4096 \(4 GB\) and 16384 \(16 GB\) in increments of 1024 \(1 GB\) \- Available `cpu` values: 2048 \(2 vCPU\)
+ Between 8192 \(8 GB\) and 30720 \(30 GB\) in increments of 1024 \(1 GB\) \- Available `cpu` values: 4096 \(4 vCPU\)
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkMode`  <a name="cfn-ecs-taskdefinition-networkmode"></a>
The Docker networking mode to use for the containers in the task\. The valid values are `none`, `bridge`, `awsvpc`, and `host`\. The default Docker network mode is `bridge`\. If you are using the Fargate launch type, the `awsvpc` network mode is required\. If you are using the EC2 launch type, any network mode can be used\. If the network mode is set to `none`, you cannot specify port mappings in your container definitions, and the tasks containers do not have external connectivity\. The `host` and `awsvpc` network modes offer the highest networking performance for containers because they use the EC2 network stack instead of the virtualized network stack provided by the `bridge` mode\.
With the `host` and `awsvpc` network modes, exposed container ports are mapped directly to the corresponding host port \(for the `host` network mode\) or the attached elastic network interface port \(for the `awsvpc` network mode\), so you cannot take advantage of dynamic host port mappings\.
If the network mode is `awsvpc`, the task is allocated an elastic network interface, and you must specify a [NetworkConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_NetworkConfiguration.html) value when you create a service or run a task with the task definition\. For more information, see [Task Networking](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-networking.html) in the *Amazon Elastic Container Service Developer Guide*\.
Currently, only Amazon ECS\-optimized AMIs, other Amazon Linux variants with the `ecs-init` package, or AWS Fargate infrastructure support the `awsvpc` network mode\.
If the network mode is `host`, you cannot run multiple instantiations of the same task on a single container instance when port mappings are used\.
Docker for Windows uses different network modes than Docker for Linux\. When you register a task definition with Windows containers, you must not specify a network mode\. If you use the console to register a task definition with Windows containers, you must choose the `<default>` network mode object\.
For more information, see [Network settings](https://docs.docker.com/engine/reference/run/#network-settings) in the *Docker run reference*\.
*Required*: No
*Type*: String
*Allowed Values*: `awsvpc | bridge | host | none`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementConstraints`  <a name="cfn-ecs-taskdefinition-placementconstraints"></a>
An array of placement constraint objects to use for tasks\. This field is not valid if you are using the Fargate launch type for your task\.
*Required*: No
*Type*: List of [TaskDefinitionPlacementConstraint](aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint.md)
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProxyConfiguration`  <a name="cfn-ecs-taskdefinition-proxyconfiguration"></a>
The `ProxyConfiguration` property specifies the configuration details for the App Mesh proxy\.
Your Amazon ECS container instances require at least version 1\.26\.0 of the container agent and at least version 1\.26\.0\-1 of the `ecs-init` package to enable a proxy configuration\. If your container instances are launched from the Amazon ECS\-optimized AMI version `20190301` or later, then they contain the required versions of the container agent and `ecs-init`\. For more information, see [Amazon ECS\-optimized Linux AMI](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No
*Type*: [ProxyConfiguration](aws-properties-ecs-taskdefinition-proxyconfiguration.md)
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RequiresCompatibilities`  <a name="cfn-ecs-taskdefinition-requirescompatibilities"></a>
The launch type the task requires\. If no value is specified, it will default to `EC2`\. Valid values include `EC2` and `FARGATE`\.
*Required*: No
*Type*: List of String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TaskRoleArn`  <a name="cfn-ecs-taskdefinition-taskrolearn"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that grants containers in the task permission to call AWS APIs on your behalf\. For more information, see [Amazon ECS Task Role](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_IAM_role.html) in the *Amazon Elastic Container Service Developer Guide*\.
IAM roles for tasks on Windows require that the `-EnableTaskIAMRole` option is set when you launch the Amazon ECS\-optimized Windows AMI\. Your containers must also run some configuration code in order to take advantage of the feature\. For more information, see [Windows IAM Roles for Tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/windows_task_IAM_roles.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Volumes`  <a name="cfn-ecs-taskdefinition-volumes"></a>
The list of volume definitions for the task\.
If your tasks are using the Fargate launch type, the `host` and `sourcePath` parameters are not supported\.
For more information about volume definition parameters and defaults, see [Amazon ECS Task Definitions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definitions.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No
*Type*: List of [Volume](aws-properties-ecs-taskdefinition-volumes.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ecs-taskdefinition-return-values"></a>

### Ref<a name="aws-resource-ecs-taskdefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\)\.

In the following example, the `Ref` function returns the ARN of the `MyTaskDefinition` task definition, such as `arn:aws:ecs:us-west-2:123456789012:task-definition/TaskDefinitionFamily:1`\.

 `{ "Ref": "MyTaskDefinition" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ecs-taskdefinition--examples"></a>

### Creating an Amazon ECS task definition<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition"></a>

The following example defines an Amazon ECS task definition, which includes two container definitions and one volume definition\.

#### JSON<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition--json"></a>

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
      "Essential": true
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
      "Essential" : false,
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

#### YAML<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition--yaml"></a>

```
taskdefinition:
  Type: AWS::ECS::TaskDefinition
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
        Essential: true
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
        Essential: false
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

### Creating an Amazon ECS task definition<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition"></a>

The following example defines an Amazon ECS task definition that specifies EC2 and FARGATE as required compatibilities\.

#### JSON<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition--json"></a>

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
            "Essential": true
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
            "Essential": false,
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

#### YAML<a name="aws-resource-ecs-taskdefinition--examples--Creating_an_Amazon_ECS_task_definition--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  taskdefinition:
    Type: AWS::ECS::TaskDefinition
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
          Essential: true
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
          Essential: false
          VolumesFrom:
            -
              SourceContainer: "my-app"
      Volumes:
        -
          Host:
            SourcePath: "/var/lib/docker/vfs/dir/"
          Name: "my-vol"
```
