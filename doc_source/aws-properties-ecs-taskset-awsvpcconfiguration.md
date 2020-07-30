# AWS::ECS::TaskSet AwsVpcConfiguration<a name="aws-properties-ecs-taskset-awsvpcconfiguration"></a>

The networking details for a task\.

## Syntax<a name="aws-properties-ecs-taskset-awsvpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskset-awsvpcconfiguration-syntax.json"></a>

```
{
  "[AssignPublicIp](#cfn-ecs-taskset-awsvpcconfiguration-assignpublicip)" : String,
  "[SecurityGroups](#cfn-ecs-taskset-awsvpcconfiguration-securitygroups)" : [ String, ... ],
  "[Subnets](#cfn-ecs-taskset-awsvpcconfiguration-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskset-awsvpcconfiguration-syntax.yaml"></a>

```
  [AssignPublicIp](#cfn-ecs-taskset-awsvpcconfiguration-assignpublicip): String
  [SecurityGroups](#cfn-ecs-taskset-awsvpcconfiguration-securitygroups): 
    - String
  [Subnets](#cfn-ecs-taskset-awsvpcconfiguration-subnets): 
    - String
```

## Properties<a name="aws-properties-ecs-taskset-awsvpcconfiguration-properties"></a>

`AssignPublicIp`  <a name="cfn-ecs-taskset-awsvpcconfiguration-assignpublicip"></a>
Whether the task's elastic network interface receives a public IP address\. The default value is `DISABLED`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-ecs-taskset-awsvpcconfiguration-securitygroups"></a>
The IDs of the security groups associated with the task or service\. If you do not specify a security group, the default security group for the VPC is used\. There is a limit of 5 security groups that can be specified per `AwsVpcConfiguration`\.  
All specified security groups must be from the same VPC\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-ecs-taskset-awsvpcconfiguration-subnets"></a>
The IDs of the subnets associated with the task or service\. There is a limit of 16 subnets that can be specified per `AwsVpcConfiguration`\.  
All specified subnets must be from the same VPC\.
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)