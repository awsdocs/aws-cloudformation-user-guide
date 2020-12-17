# AWS::OpsWorks::App EnvironmentVariable<a name="aws-properties-opsworks-app-environment"></a>

Represents an app's environment variable\.

## Syntax<a name="aws-properties-opsworks-app-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-app-environment-syntax.json"></a>

```
{
  "[Key](#cfn-opsworks-app-environment-key)" : String,
  "[Secure](#cfn-opsworks-app-environment-secure)" : Boolean,
  "[Value](#value)" : String
}
```

### YAML<a name="aws-properties-opsworks-app-environment-syntax.yaml"></a>

```
  [Key](#cfn-opsworks-app-environment-key): String
  [Secure](#cfn-opsworks-app-environment-secure): Boolean
  [Value](#value): String
```

## Properties<a name="aws-properties-opsworks-app-environment-properties"></a>

`Key`  <a name="cfn-opsworks-app-environment-key"></a>
\(Required\) The environment variable's name, which can consist of up to 64 characters and must be specified\. The name can contain upper\- and lowercase letters, numbers, and underscores \(\_\), but it must start with a letter or underscore\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Secure`  <a name="cfn-opsworks-app-environment-secure"></a>
\(Optional\) Whether the variable's value will be returned by the [DescribeApps](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/DescribeApps) action\. To conceal an environment variable's value, set `Secure` to `true`\. `DescribeApps` then returns `*****FILTERED*****` instead of the actual value\. The default value for `Secure` is `false`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="value"></a>
\(Optional\) The environment variable's value, which can be left empty\. If you specify a value, it can contain up to 256 characters, which must all be printable\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)