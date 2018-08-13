# AWS Elastic Beanstalk Environment OptionSetting<a name="aws-properties-beanstalk-option-settings"></a>

The `OptionSetting` property type specifies an option for an AWS Elastic Beanstalk environment\.

The `OptionSettings` property of the [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md) resource contains a list of `OptionSetting` property types\.

## Syntax<a name="w3ab2c21c14d954b7"></a>

### JSON<a name="aws-properties-beanstalk-option-settings-syntax.json"></a>

```
{
   "[Namespace](#cfn-beanstalk-optionsettings-namespace)" : String,
   "[OptionName](#cfn-beanstalk-optionsettings-optionname)" : String,
   "[ResourceName](#cfn-elasticbeanstalk-environment-optionsetting-resourcename)" : String,
   "[Value](#cfn-beanstalk-optionsettings-value)" : String
}
```

### YAML<a name="aws-properties-beanstalk-option-settings-syntax.yaml"></a>

```
[Namespace](#cfn-beanstalk-optionsettings-namespace): String
[OptionName](#cfn-beanstalk-optionsettings-optionname): String
[ResourceName](#cfn-elasticbeanstalk-environment-optionsetting-resourcename): String
[Value](#cfn-beanstalk-optionsettings-value): String
```

## Properties<a name="w3ab2c21c14d954b9"></a>

`Namespace`  <a name="cfn-beanstalk-optionsettings-namespace"></a>
A unique namespace that identifies the option's associated AWS resource\. For a list of namespaces that you can use, see [Configuration Options](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required*: Yes  
*Type*: String

`OptionName`  <a name="cfn-beanstalk-optionsettings-optionname"></a>
The name of the configuration option\. For a list of options that you can use, see [Configuration Options](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required*: Yes  
*Type*: String

`ResourceName`  <a name="cfn-elasticbeanstalk-environment-optionsetting-resourcename"></a>
A unique resource name for the option setting\. Use this property for a time–based scaling configuration option\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-beanstalk-optionsettings-value"></a>
The current value for the configuration option\.  
*Required*: No  
*Type*: String

## See Also<a name="w3ab2c21c14d954c11"></a>
+ [ConfigurationOptionSetting](http://docs.aws.amazon.com//elasticbeanstalk/latest/api/API_ConfigurationOptionSetting.html) in the *AWS Elastic Beanstalk Developer Guide*
+ [Option Values](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*