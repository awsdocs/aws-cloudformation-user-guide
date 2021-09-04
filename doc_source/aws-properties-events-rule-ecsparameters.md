# AWS::Events::Rule EcsParameters<a name="aws-properties-events-rule-ecsparameters"></a>

The custom parameters to be used when the target is an Amazon ECS task\.

## Syntax<a name="aws-properties-events-rule-ecsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-ecsparameters-syntax.json"></a>

```
{
  "[Group](#cfn-events-rule-ecsparameters-group)" : String,
  "[LaunchType](#cfn-events-rule-ecsparameters-launchtype)" : String,
  "[NetworkConfiguration](#cfn-events-rule-ecsparameters-networkconfiguration)" : NetworkConfiguration,
  "[PlatformVersion](#cfn-events-rule-ecsparameters-platformversion)" : String,
  "[TaskCount](#cfn-events-rule-ecsparameters-taskcount)" : Integer,
  "[TaskDefinitionArn](#cfn-events-rule-ecsparameters-taskdefinitionarn)" : String
}
```

### YAML<a name="aws-properties-events-rule-ecsparameters-syntax.yaml"></a>

```
  [Group](#cfn-events-rule-ecsparameters-group): String
  [LaunchType](#cfn-events-rule-ecsparameters-launchtype): String
  [NetworkConfiguration](#cfn-events-rule-ecsparameters-networkconfiguration): 
    NetworkConfiguration
  [PlatformVersion](#cfn-events-rule-ecsparameters-platformversion): String
  [TaskCount](#cfn-events-rule-ecsparameters-taskcount): Integer
  [TaskDefinitionArn](#cfn-events-rule-ecsparameters-taskdefinitionarn): String
```

## Properties<a name="aws-properties-events-rule-ecsparameters-properties"></a>

`Group`  <a name="cfn-events-rule-ecsparameters-group"></a>
Specifies an ECS task group for the task\. The maximum length is 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchType`  <a name="cfn-events-rule-ecsparameters-launchtype"></a>
Specifies the launch type on which your task is running\. The launch type that you specify here must match one of the launch type \(compatibilities\) of the target task\. The `FARGATE` value is supported only in the Regions where AWS Fargate witt Amazon ECS is supported\. For more information, see [ AWS Fargate on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS-Fargate.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EC2 | EXTERNAL | FARGATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkConfiguration`  <a name="cfn-events-rule-ecsparameters-networkconfiguration"></a>
Use this structure if the Amazon ECS task uses the `awsvpc` network mode\. This structure specifies the VPC subnets and security groups associated with the task, and whether a public IP address is to be used\. This structure is required if `LaunchType` is `FARGATE` because the `awsvpc` mode is required for Fargate tasks\.  
If you specify `NetworkConfiguration` when the target ECS task does not use the `awsvpc` network mode, the task fails\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-events-rule-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlatformVersion`  <a name="cfn-events-rule-ecsparameters-platformversion"></a>
Specifies the platform version for the task\. Specify only the numeric portion of the platform version, such as `1.1.0`\.  
This structure is used only if `LaunchType` is `FARGATE`\. For more information about valid platform versions, see [ AWS Fargate Platform Versions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/platform_versions.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskCount`  <a name="cfn-events-rule-ecsparameters-taskcount"></a>
The number of tasks to create based on `TaskDefinition`\. The default is 1\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskDefinitionArn`  <a name="cfn-events-rule-ecsparameters-taskdefinitionarn"></a>
The ARN of the task definition to use if the event target is an Amazon ECS task\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-events-rule-ecsparameters--examples"></a>



### <a name="aws-properties-events-rule-ecsparameters--examples--"></a>

The following example defines the ECS parameters\.

#### JSON<a name="aws-properties-events-rule-ecsparameters--examples----json"></a>

```
{
  "LaunchType": "FARGATE",
  "NetworkConfiguration": {
    "AwsVpcConfiguration": {
      "AssignPublicIp": "DISABLED",
      "SecurityGroups": [
        {
          "Fn: : GetAtt": [
            "ScheduledFargateTaskScheduledTaskDefSecurityGroupE075BC19",
            "GroupId"
          ]
        }
      ],
      "Subnets": [
        {
          "Ref": "VpcPrivateSubnet1Subnet536B997A"
        }
      ]
    }
  },
  "TaskCount": 2,
  "TaskDefinitionArn": {
     "Ref": "ScheduledFargateTaskScheduledTaskDef521FA675"
  },
  "enableECSManagedTags": true,
  "placementConstraints": [ 
    { 
        "expression": "attribute:ecs.instance-type == t2.small",
        "type": "memberOf"
    }
  ],
  "placementStrategy": [ 
  { 
     "field": "instanceId",
     "type ": "binpack"
  }
  ],
  "propagateTags": "TASK_DEFINITION",
  "referenceId": "idopsks",
  "startedBy": "surearu",
  "tags": [ 
      { 
          "key": "maintask",
          "value ": "taskvalue"
      }
  ]
}
```

#### YAML<a name="aws-properties-events-rule-ecsparameters--examples----yaml"></a>

```
LaunchType: "FARGATE"
NetworkConfiguration:
  AwsVpcConfiguration:
    AssignPublicIp: "DISABLED"
    SecurityGroups:
      Fn: : GetAtt:
        "ScheduledFargateTaskScheduledTaskDefSecurityGroupE075BC19",
        "GroupId"
    Subnets:
      Ref: 
        "VpcPrivateSubnet1Subnet536B997A"
TaskCount: 2
TaskDefinitionArn:
  Ref: 
    "ScheduledFargateTaskScheduledTaskDef521FA675"
enableECSManagedTags: true
placementConstraints:  
  expression: 
    "attribute:ecs.instance-type == t2.small"
  type: 
    "memberOf"
placementStrategy: 
  field: 
    "instanceId"
  type: 
    "binpack"
propagateTags: 
  "TASK_DEFINITION"
referenceId: 
  "idopsks"
startedBy: 
  "surearu"
tags:
  key: 
    "maintask"
  value: 
    "taskvalue"
```