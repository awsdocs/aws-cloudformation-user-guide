# AWS::ECS::TaskDefinition KeyValuePair<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment"></a>

The `KeyValuePair` property specifies a key\-value pair object\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-syntax.json"></a>

```
{
  "[Name](#cfn-ecs-taskdefinition-containerdefinition-environment-name)" : String,
  "[Value](#cfn-ecs-taskdefinition-containerdefinition-environment-value)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-syntax.yaml"></a>

```
  [Name](#cfn-ecs-taskdefinition-containerdefinition-environment-name): String
  [Value](#cfn-ecs-taskdefinition-containerdefinition-environment-value): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-properties"></a>

`Name`  <a name="cfn-ecs-taskdefinition-containerdefinition-environment-name"></a>
The name of the key\-value pair\. For environment variables, this is the name of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-ecs-taskdefinition-containerdefinition-environment-value"></a>
The value of the key\-value pair\. For environment variables, this is the value of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)