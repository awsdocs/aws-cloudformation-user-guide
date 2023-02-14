# AWS::Lightsail::Instance State<a name="aws-properties-lightsail-instance-state"></a>

`State` is a property of the [AWS::Lightsail::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-instance.html) resource\. It describes the status code and the state \(for example, `running`\) of an instance\.

## Syntax<a name="aws-properties-lightsail-instance-state-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-state-syntax.json"></a>

```
{
  "[Code](#cfn-lightsail-instance-state-code)" : Integer,
  "[Name](#cfn-lightsail-instance-state-name)" : String
}
```

### YAML<a name="aws-properties-lightsail-instance-state-syntax.yaml"></a>

```
  [Code](#cfn-lightsail-instance-state-code): Integer
  [Name](#cfn-lightsail-instance-state-name): String
```

## Properties<a name="aws-properties-lightsail-instance-state-properties"></a>

`Code`  <a name="cfn-lightsail-instance-state-code"></a>
The status code of the instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lightsail-instance-state-name"></a>
The state of the instance \(for example, `running` or `pending`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)