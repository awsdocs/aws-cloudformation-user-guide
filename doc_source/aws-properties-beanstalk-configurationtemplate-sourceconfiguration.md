# AWS Elastic Beanstalk ConfigurationTemplate SourceConfiguration<a name="aws-properties-beanstalk-configurationtemplate-sourceconfiguration"></a>

Use settings from another Elastic Beanstalk configuration template for the [AWS::ElasticBeanstalk::ConfigurationTemplate](aws-resource-beanstalk-configurationtemplate.md) resource type\.

## Syntax<a name="w3ab2c21c14d759b5"></a>

### JSON<a name="aws-properties-beanstalk-configurationtemplate-sourceconfiguration-syntax.json"></a>

```
{
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-beanstalk-configurationtemplate-sourceconfiguration-applicationname)" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-beanstalk-configurationtemplate-sourceconfiguration-templatename)" : String
}
```

### YAML<a name="aws-properties-beanstalk-configurationtemplate-sourceconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-beanstalk-configurationtemplate-sourceconfiguration-applicationname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-beanstalk-configurationtemplate-sourceconfiguration-templatename): String
```

## Properties<a name="w3ab2c21c14d759b7"></a>

`ApplicationName`  
The name of the Elastic Beanstalk application that contains the configuration template that you want to use\.  
*Required: *Yes  
*Type*: String

`TemplateName`  
The name of the configuration template\.  
*Required: *Yes  
*Type*: String