# AWS::ECS::Service NetworkConfiguration<a name="aws-properties-ecs-service-networkconfiguration"></a>

The `NetworkConfiguration` property specifies an object representing the network configuration for a task or service\.

## Syntax<a name="aws-properties-ecs-service-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-networkconfiguration-syntax.json"></a>

```
{
  "[AwsvpcConfiguration](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration)" : AwsVpcConfiguration
}
```

### YAML<a name="aws-properties-ecs-service-networkconfiguration-syntax.yaml"></a>

```
  [AwsvpcConfiguration](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration): 
    AwsVpcConfiguration
```

## Properties<a name="aws-properties-ecs-service-networkconfiguration-properties"></a>

`AwsvpcConfiguration`  <a name="cfn-ecs-service-networkconfiguration-awsvpcconfiguration"></a>
The VPC subnets and security groups associated with a task\.  
All specified subnets and security groups must be from the same VPC\.
*Required*: No  
*Type*: [AwsVpcConfiguration](aws-properties-ecs-service-awsvpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)