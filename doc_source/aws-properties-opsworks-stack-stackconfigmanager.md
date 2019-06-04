# AWS::OpsWorks::Stack StackConfigurationManager<a name="aws-properties-opsworks-stack-stackconfigmanager"></a>

Describes the configuration manager\.

## Syntax<a name="aws-properties-opsworks-stack-stackconfigmanager-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-opsworks-stack-stackconfigmanager-properties"></a>

`Name`  <a name="cfn-opsworks-configmanager-name"></a>
The name\. This parameter must be set to "Chef"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-opsworks-configmanager-version"></a>
The Chef version\. This parameter must be set to 12, 11\.10, or 11\.4 for Linux stacks, and to 12\.2 for Windows stacks\. The default value for Linux stacks is 11\.4\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)