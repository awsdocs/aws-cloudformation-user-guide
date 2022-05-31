# AWS::Lightsail::Container EnvironmentVariable<a name="aws-properties-lightsail-container-environmentvariable"></a>

`EnvironmentVariable` is a property of the [Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-container-container.html) property\. It describes the environment variables of a container on a container service which are key\-value parameters that provide dynamic configuration of the application or script run by the container\.

## Syntax<a name="aws-properties-lightsail-container-environmentvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-container-environmentvariable-syntax.json"></a>

```
{
  "[Value](#cfn-lightsail-container-environmentvariable-value)" : String,
  "[Variable](#cfn-lightsail-container-environmentvariable-variable)" : String
}
```

### YAML<a name="aws-properties-lightsail-container-environmentvariable-syntax.yaml"></a>

```
  [Value](#cfn-lightsail-container-environmentvariable-value): String
  [Variable](#cfn-lightsail-container-environmentvariable-variable): String
```

## Properties<a name="aws-properties-lightsail-container-environmentvariable-properties"></a>

`Value`  <a name="cfn-lightsail-container-environmentvariable-value"></a>
The environment variable value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variable`  <a name="cfn-lightsail-container-environmentvariable-variable"></a>
The environment variable key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)