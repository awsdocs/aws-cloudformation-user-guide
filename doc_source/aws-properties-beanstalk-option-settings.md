# AWS Elastic Beanstalk Environment OptionSetting<a name="aws-properties-beanstalk-option-settings"></a>

The `OptionSetting` property type specifies an option for an AWS Elastic Beanstalk environment\.

The `OptionSettings` property of the [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md) resource contains a list of `OptionSetting` property types\.

## Syntax<a name="w3ab2c21c14d767b7"></a>

### JSON<a name="aws-properties-beanstalk-option-settings-syntax.json"></a>

```
{
   "Namespace" : String,
   "OptionName" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-environment-optionsetting-resourcename)" : String,
   "Value" : String
}
```

### YAML<a name="aws-properties-beanstalk-option-settings-syntax.yaml"></a>

```
Namespace: String
OptionName: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-environment-optionsetting-resourcename): String
Value: String
```

## Properties<a name="w3ab2c21c14d767b9"></a>

`Namespace`  
A unique namespace that identifies the option's associated AWS resource\. For a list of namespaces that you can use, see [Configuration Options](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required: *Yes  
*Type*: String

`OptionName`  
The name of the configuration option\. For a list of options that you can use, see [Configuration Options](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required: *Yes  
*Type*: String

`ResourceName`  
A unique resource name for the option setting\. Use this property for a time–based scaling configuration option\.  
*Required*: No  
*Type*: String

`Value`  
The current value for the configuration option\.  
*Required: *No  
*Type*: String

## See Also<a name="w3ab2c21c14d767c11"></a>

+ [ConfigurationOptionSetting](http://docs.aws.amazon.com//elasticbeanstalk/latest/api/API_ConfigurationOptionSetting.html) in the *AWS Elastic Beanstalk Developer Guide*

+ [Option Values](http://docs.aws.amazon.com//elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*