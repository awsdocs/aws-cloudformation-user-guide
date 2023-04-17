# AWS::AppConfig::Extension Parameter<a name="aws-properties-appconfig-extension-parameter"></a>

A value such as an Amazon Resource Name \(ARN\) or an Amazon Simple Notification Service topic entered in an extension when invoked\. Parameter values are specified in an extension association\. For more information about extensions, see [Working with AWS AppConfig extensions](https://docs.aws.amazon.com/appconfig/latest/userguide/working-with-appconfig-extensions.html) in the * AWS AppConfig User Guide*\.

## Syntax<a name="aws-properties-appconfig-extension-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appconfig-extension-parameter-syntax.json"></a>

```
{
  "[Description](#cfn-appconfig-extension-parameter-description)" : String,
  "[Required](#cfn-appconfig-extension-parameter-required)" : Boolean
}
```

### YAML<a name="aws-properties-appconfig-extension-parameter-syntax.yaml"></a>

```
  [Description](#cfn-appconfig-extension-parameter-description): String
  [Required](#cfn-appconfig-extension-parameter-required): Boolean
```

## Properties<a name="aws-properties-appconfig-extension-parameter-properties"></a>

`Description`  <a name="cfn-appconfig-extension-parameter-description"></a>
Information about the parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Required`  <a name="cfn-appconfig-extension-parameter-required"></a>
A parameter value must be specified in the extension association\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)