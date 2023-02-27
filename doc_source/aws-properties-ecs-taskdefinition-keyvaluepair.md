# AWS::ECS::TaskDefinition KeyValuePair<a name="aws-properties-ecs-taskdefinition-keyvaluepair"></a>

The `KeyValuePair` property specifies a key\-value pair object\.

## Syntax<a name="aws-properties-ecs-taskdefinition-keyvaluepair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-keyvaluepair-syntax.json"></a>

```
{
  "[Name](#cfn-ecs-taskdefinition-keyvaluepair-name)" : String,
  "[Value](#cfn-ecs-taskdefinition-keyvaluepair-value)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-keyvaluepair-syntax.yaml"></a>

```
  [Name](#cfn-ecs-taskdefinition-keyvaluepair-name): String
  [Value](#cfn-ecs-taskdefinition-keyvaluepair-value): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-keyvaluepair-properties"></a>

`Name`  <a name="cfn-ecs-taskdefinition-keyvaluepair-name"></a>
The name of the key\-value pair\. For environment variables, this is the name of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-ecs-taskdefinition-keyvaluepair-value"></a>
The value of the key\-value pair\. For environment variables, this is the value of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)