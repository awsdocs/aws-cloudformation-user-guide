# AWS OpsWorks App Environment<a name="aws-properties-opsworks-app-environment"></a>

`Environment` is a property of the [AWS::OpsWorks::App](aws-resource-opsworks-app.md) resource that specifies the environment variable to associate with the AWS OpsWorks app\.

## Syntax<a name="w3ab2c21c14e1549b5"></a>

### JSON<a name="aws-properties-opsworks-app-environment-syntax.json"></a>

```
{
  "[Key](#cfn-opsworks-app-environment-key)" : String,
  "[Secure](#cfn-opsworks-app-environment-secure)" : Boolean,
  "[Value](#cfn-opsworks-app-environment-value)" : String
}
```

### YAML<a name="aws-properties-opsworks-app-environment-syntax.yaml"></a>

```
[Key](#cfn-opsworks-app-environment-key): String
[Secure](#cfn-opsworks-app-environment-secure): Boolean
[Value](#cfn-opsworks-app-environment-value): String
```

## Properties<a name="w3ab2c21c14e1549b7"></a>

`Key`  <a name="cfn-opsworks-app-environment-key"></a>
The name of the environment variable, which can consist of up to 64 characters\. You can use upper and lowercase letters, numbers, and underscores \(\_\), but the name must start with a letter or underscore\.  
*Required*: Yes  
*Type*: String

`Secure`  <a name="cfn-opsworks-app-environment-secure"></a>
Indicates whether the value of the environment variable is concealed, such as with a [DescribeApps](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_DescribeApps.html) response\. To conceal an environment variable's value, set the value to `true`\.  
*Required*: No  
*Type*: Boolean

`Value`  <a name="cfn-opsworks-app-environment-value"></a>
The value of the environment variable, which can be empty\. You can specify a value of up to 256 characters\.  
*Required*: Yes  
*Type*: String