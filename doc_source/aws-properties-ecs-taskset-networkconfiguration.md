# AWS::ECS::TaskSet NetworkConfiguration<a name="aws-properties-ecs-taskset-networkconfiguration"></a>

The network configuration for a task\.

## Syntax<a name="aws-properties-ecs-taskset-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskset-networkconfiguration-syntax.json"></a>

```
{
  "[AwsVpcConfiguration](#cfn-ecs-taskset-networkconfiguration-awsvpcconfiguration)" : AwsVpcConfiguration
}
```

### YAML<a name="aws-properties-ecs-taskset-networkconfiguration-syntax.yaml"></a>

```
  [AwsVpcConfiguration](#cfn-ecs-taskset-networkconfiguration-awsvpcconfiguration): 
    AwsVpcConfiguration
```

## Properties<a name="aws-properties-ecs-taskset-networkconfiguration-properties"></a>

`AwsVpcConfiguration`  <a name="cfn-ecs-taskset-networkconfiguration-awsvpcconfiguration"></a>
The VPC subnets and security groups associated with a task\.  
All specified subnets and security groups must be from the same VPC\.
*Required*: No  
*Type*: [AwsVpcConfiguration](aws-properties-ecs-taskset-awsvpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)