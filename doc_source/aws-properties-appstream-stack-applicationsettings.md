# Amazon AppStream 2\.0 Stack ApplicationSettings<a name="aws-properties-appstream-stack-applicationsettings"></a>

<a name="aws-properties-appstream-stack-applicationsettings-description"></a>The `ApplicationSettings` property type specifies the persistent application settings for users of an Amazon AppStream 2\.0 stack\.

<a name="aws-properties-appstream-stack-applicationsettings-inheritance"></a> `ApplicationSettings` is a property of the [AWS::AppStream::Stack](aws-resource-appstream-stack.md) resource type\.

## Syntax<a name="aws-properties-appstream-stack-applicationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-stack-applicationsettings-syntax.json"></a>

```
{
  "[Enabled](#cfn-appstream-stack-applicationsettings-enabled)" : Boolean,
  "[SettingsGroup](#cfn-appstream-stack-applicationsettings-settingsgroup)" : String
}
```

### YAML<a name="aws-properties-appstream-stack-applicationsettings-syntax.yaml"></a>

```
[Enabled](#cfn-appstream-stack-applicationsettings-enabled): Boolean
[SettingsGroup](#cfn-appstream-stack-applicationsettings-settingsgroup): String
```

## Properties<a name="aws-properties-appstream-stack-applicationsettings-properties"></a>

`Enabled`  <a name="cfn-appstream-stack-applicationsettings-enabled"></a>
Specifies whether persistent application settings are enabled for users during their streaming sessions\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SettingsGroup`  <a name="cfn-appstream-stack-applicationsettings-settingsgroup"></a>
The path prefix for the Amazon S3 bucket where users’ persistent application settings are stored\. You can allow the same persistent application settings to be used across multiple stacks by specifying the same settings group for each stack\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 