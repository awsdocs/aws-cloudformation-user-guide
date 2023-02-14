# AWS::ECS::TaskDefinition Ulimit<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit"></a>

The `Ulimit` property specifies the `ulimit` settings to pass to the container\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-syntax.json"></a>

```
{
  "[HardLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit)" : Integer,
  "[Name](#cfn-ecs-taskdefinition-containerdefinition-ulimit-name)" : String,
  "[SoftLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-syntax.yaml"></a>

```
  [HardLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit): Integer
  [Name](#cfn-ecs-taskdefinition-containerdefinition-ulimit-name): String
  [SoftLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit): Integer
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-properties"></a>

`HardLimit`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit"></a>
The hard limit for the ulimit type\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-name"></a>
The `type` of the `ulimit`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `core | cpu | data | fsize | locks | memlock | msgqueue | nice | nofile | nproc | rss | rtprio | rttime | sigpending | stack`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SoftLimit`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit"></a>
The soft limit for the ulimit type\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)