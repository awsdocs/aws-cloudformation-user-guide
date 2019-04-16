# AWS OpsWorks StackConfigurationManager Type<a name="aws-properties-opsworks-stack-stackconfigmanager"></a>

Describes the stack configuration manager for the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) resource type\. For more information, see [StackConfigurationManager](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_StackConfigurationManager.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w13ab1c21c10d183c38c29b5"></a>

### JSON<a name="aws-properties-opsworks-stack-stackconfigmanager-syntax.json"></a>

```
{
  "[Name](#cfn-opsworks-configmanager-name)" : String,
  "[Version](#cfn-opsworks-configmanager-version)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-stackconfigmanager-syntax.yaml"></a>

```
[Name](#cfn-opsworks-configmanager-name): String
[Version](#cfn-opsworks-configmanager-version): String
```

## Properties<a name="w13ab1c21c10d183c38c29b7"></a>

`Name`  <a name="cfn-opsworks-configmanager-name"></a>
The name of the configuration manager\.  
*Required*: No  
*Type*: String

`Version`  <a name="cfn-opsworks-configmanager-version"></a>
The Chef version\.  
*Required*: No  
*Type*: String