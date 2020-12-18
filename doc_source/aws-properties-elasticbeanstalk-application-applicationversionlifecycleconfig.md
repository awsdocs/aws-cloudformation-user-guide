# AWS::ElasticBeanstalk::Application ApplicationVersionLifecycleConfig<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig"></a>

The application version lifecycle settings for an application\. Defines the rules that Elastic Beanstalk applies to an application's versions in order to avoid hitting the per\-region limit for application versions\.

When Elastic Beanstalk deletes an application version from its database, you can no longer deploy that version to an environment\. The source bundle remains in S3 unless you configure the rule to delete it\.

 `ApplicationVersionLifecycleConfig` is a property of the [ApplicationResourceLifecycleConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.html) property type\.

## Syntax<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax.json"></a>

```
{
  "[MaxAgeRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule)" : MaxAgeRule,
  "[MaxCountRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule)" : MaxCountRule
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-syntax.yaml"></a>

```
  [MaxAgeRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule): 
    MaxAgeRule
  [MaxCountRule](#cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule): 
    MaxCountRule
```

## Properties<a name="aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig-properties"></a>

`MaxAgeRule`  <a name="cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxagerule"></a>
Specify a max age rule to restrict the length of time that application versions are retained for an application\.  
*Required*: No  
*Type*: [MaxAgeRule](aws-properties-elasticbeanstalk-application-maxagerule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCountRule`  <a name="cfn-elasticbeanstalk-application-applicationversionlifecycleconfig-maxcountrule"></a>
Specify a max count rule to restrict the number of application versions that are retained for an application\.  
*Required*: No  
*Type*: [MaxCountRule](aws-properties-elasticbeanstalk-application-maxcountrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)