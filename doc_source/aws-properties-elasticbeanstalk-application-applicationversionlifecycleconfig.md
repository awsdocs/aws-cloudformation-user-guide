# AWS Elastic Beanstalk Application ApplicationVersionLifecycleConfig<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig"></a>

<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-description"></a>The `ApplicationVersionLifecycleConfig` property type specifies the application version lifecycle settings for an AWS Elastic Beanstalk application\. It defines the rules that Elastic Beanstalk applies to an application's versions in order to avoid hitting the per\-region limit for application versions\.

When Elastic Beanstalk deletes an application version from its database, you can no longer deploy that version to an environment\. The source bundle remains in S3 unless you configure the rule to delete it\.

<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-inheritance"></a> `ApplicationVersionLifecycleConfig` is a property of the [Elastic Beanstalk Application ApplicationResourceLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md) property type\. 

## Syntax<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax.json"></a>

```
{
  "[MaxAgeRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule)" : [*MaxAgeRule*](aws-properties-elasticbeanstalk-application-maxagerule.md),
  "[MaxCountRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule)" : [*MaxCountRule*](aws-properties-elasticbeanstalk-application-maxcountrule.md)
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax.yaml"></a>

```
[MaxAgeRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule): MaxAgeRule
[MaxCountRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule): MaxCountRule
```

## Properties<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-properties"></a>

`MaxAgeRule`  <a name="cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule"></a>
Specifies a max age rule to restrict the length of time that application versions are retained for an application\.  
 *Required*: No  
 *Type*: [Elastic Beanstalk Application MaxAgeRule](aws-properties-elasticbeanstalk-application-maxagerule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxCountRule`  <a name="cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule"></a>
Specifies a max count rule to restrict the number of application versions that are retained for an application\.  
 *Required*: No  
 *Type*: [Elastic Beanstalk Application MaxCountRule](aws-properties-elasticbeanstalk-application-maxcountrule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 