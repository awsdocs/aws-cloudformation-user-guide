# AWS Elastic Beanstalk ConfigurationTemplate ConfigurationOptionSetting<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting"></a>

The `ConfigurationOptionSetting` property type specifies an option for an AWS Elastic Beanstalk configuration template\.

The `OptionSettings` property of the [AWS::ElasticBeanstalk::ConfigurationTemplate](aws-resource-beanstalk-configurationtemplate.md) resource contains a list of `ConfigurationOptionSetting` property types\.

## Syntax<a name="w3ab2c21c14d942b7"></a>

### JSON<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting-syntax.json"></a>

```
{
   "[Namespace](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-namespace)" : String,
   "[OptionName](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-optionname)" : String,
   "[ResourceName](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-resourcename)" : String,
   "[Value](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-value)" : String
}
```

### YAML<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting-syntax.yaml"></a>

```
[Namespace](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-namespace): String
[OptionName](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-optionname): String
[ResourceName](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-resourcename): String
[Value](#cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-value): String
```

## Properties<a name="w3ab2c21c14d942b9"></a>

`Namespace`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-namespace"></a>
A unique namespace that identifies the option's associated AWS resource\. For a list of namespaces that you can use, see [Configuration Options](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required*: Yes  
*Type*: String

`OptionName`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-optionname"></a>
The name of the configuration option\. For a list of options that you can use, see [Configuration Options](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required*: Yes  
*Type*: String

`ResourceName`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-resourcename"></a>
A unique resource name for the option setting\. Use this property for a time–based scaling configuration option\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-value"></a>
The current value for the configuration option\.  
*Required*: No  
*Type*: String

## See Also<a name="w3ab2c21c14d942c11"></a>
+ [ConfigurationOptionSetting](http://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_ConfigurationOptionSetting.html) in the *AWS Elastic Beanstalk Developer Guide*
+ [Configuration Options](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*