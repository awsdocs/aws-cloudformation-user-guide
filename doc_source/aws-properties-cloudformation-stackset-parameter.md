# AWS::CloudFormation::StackSet Parameter<a name="aws-properties-cloudformation-stackset-parameter"></a>

The Parameter data type\.

## Syntax<a name="aws-properties-cloudformation-stackset-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-parameter-syntax.json"></a>

```
{
  "[ParameterKey](#cfn-cloudformation-stackset-parameter-parameterkey)" : String,
  "[ParameterValue](#cfn-cloudformation-stackset-parameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-cloudformation-stackset-parameter-syntax.yaml"></a>

```
  [ParameterKey](#cfn-cloudformation-stackset-parameter-parameterkey): String
  [ParameterValue](#cfn-cloudformation-stackset-parameter-parametervalue): String
```

## Properties<a name="aws-properties-cloudformation-stackset-parameter-properties"></a>

`ParameterKey`  <a name="cfn-cloudformation-stackset-parameter-parameterkey"></a>
The key associated with the parameter\. If you don't specify a key and value for a particular parameter, AWS CloudFormation uses the default value that is specified in your template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValue`  <a name="cfn-cloudformation-stackset-parameter-parametervalue"></a>
The input value associated with the parameter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)