# AWS::ElasticBeanstalk::ConfigurationTemplate SourceConfiguration<a name="aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration"></a>

An AWS Elastic Beanstalk configuration template to base a new one on\. You can use it to define a [AWS::ElasticBeanstalk::ConfigurationTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-beanstalk-configurationtemplate.html) resource\.

## Syntax<a name="aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration-syntax.json"></a>

```
{
  "[ApplicationName](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-applicationname)" : String,
  "[TemplateName](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-templatename)" : String
}
```

### YAML<a name="aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration-syntax.yaml"></a>

```
  [ApplicationName](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-applicationname): String
  [TemplateName](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-templatename): String
```

## Properties<a name="aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration-properties"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-applicationname"></a>
The name of the application associated with the configuration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration-templatename"></a>
The name of the configuration template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)