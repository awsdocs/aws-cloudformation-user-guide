# AWS::Events::Rule AwsVpcConfiguration<a name="aws-properties-events-rule-awsvpcconfiguration"></a>

This structure specifies the VPC subnets and security groups for the task, and whether a public IP address is to be used\. This structure is relevant only for ECS tasks that use the `awsvpc` network mode\.

## Syntax<a name="aws-properties-events-rule-awsvpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-awsvpcconfiguration-syntax.json"></a>

```
{
  "[AssignPublicIp](#cfn-events-rule-awsvpcconfiguration-assignpublicip)" : String,
  "[SecurityGroups](#cfn-events-rule-awsvpcconfiguration-securitygroups)" : [ String, ... ],
  "[Subnets](#cfn-events-rule-awsvpcconfiguration-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-events-rule-awsvpcconfiguration-syntax.yaml"></a>

```
  [AssignPublicIp](#cfn-events-rule-awsvpcconfiguration-assignpublicip): String
  [SecurityGroups](#cfn-events-rule-awsvpcconfiguration-securitygroups): 
    - String
  [Subnets](#cfn-events-rule-awsvpcconfiguration-subnets): 
    - String
```

## Properties<a name="aws-properties-events-rule-awsvpcconfiguration-properties"></a>

`AssignPublicIp`  <a name="cfn-events-rule-awsvpcconfiguration-assignpublicip"></a>
Specifies whether the task's elastic network interface receives a public IP address\. You can specify `ENABLED` only when `LaunchType` in `EcsParameters` is set to `FARGATE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroups`  <a name="cfn-events-rule-awsvpcconfiguration-securitygroups"></a>
Specifies the security groups associated with the task\. These security groups must all be in the same VPC\. You can specify as many as five security groups\. If you do not specify a security group, the default security group for the VPC is used\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnets`  <a name="cfn-events-rule-awsvpcconfiguration-subnets"></a>
Specifies the subnets associated with the task\. These subnets must all be in the same VPC\. You can specify as many as 16 subnets\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-events-rule-awsvpcconfiguration--seealso"></a>
+ [AwsVpcConfiguration](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_AwsVpcConfiguration.html)