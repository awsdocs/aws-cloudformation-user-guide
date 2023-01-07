# AWS::ElasticBeanstalk::ConfigurationTemplate ConfigurationOptionSetting<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting"></a>

The `ConfigurationOptionSetting` property type specifies an option for an AWS Elastic Beanstalk configuration template\.

The `OptionSettings` property of the [AWS::ElasticBeanstalk::ConfigurationTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-beanstalk-configurationtemplate.html) resource contains a list of `ConfigurationOptionSetting` property types\.

For a list of possible namespaces and option values, see [Option Values](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.

## Syntax<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting-properties"></a>

`Namespace`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-namespace"></a>
A unique namespace that identifies the option's associated AWS resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionName`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-optionname"></a>
The name of the configuration option\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceName`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-resourcename"></a>
A unique resource name for the option setting\. Use it for a time–based scaling configuration option\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-elasticbeanstalk-configurationtemplate-configurationoptionsetting-value"></a>
The current value for the configuration option\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting--seealso"></a>
+  [ConfigurationOptionSetting](https://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_ConfigurationOptionSetting.html) in the *AWS Elastic Beanstalk API Reference* 
+  [Configuration Options](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide* 