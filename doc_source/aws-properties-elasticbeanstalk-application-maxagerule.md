# AWS Elastic Beanstalk Application MaxAgeRule<a name="aws-properties-elasticbeanstalk-application-maxagerule"></a>

<a name="aws-properties-elasticbeanstalk-application-maxagerule-description"></a>The `MaxAgeRule` property type specifies a lifecycle rule that deletes application versions after the specified number of days for an AWS Elastic Beanstalk application\.

<a name="aws-properties-elasticbeanstalk-application-maxagerule-inheritance"></a> `MaxAgeRule` is a property of the [Elastic Beanstalk Application ApplicationVersionLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.md) property type\. 

## Syntax<a name="aws-properties-elasticbeanstalk-application-maxagerule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-maxagerule-syntax.json"></a>

```
{
  "[DeleteSourceFromS3](#cfn-elasticbeanstalk-application-maxagerule-deletesourcefroms3)" : Boolean,
  "[Enabled](#cfn-elasticbeanstalk-application-maxagerule-enabled)" : Boolean,
  "[MaxAgeInDays](#cfn-elasticbeanstalk-application-maxagerule-maxageindays)" : Integer
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-maxagerule-syntax.yaml"></a>

```
[DeleteSourceFromS3](#cfn-elasticbeanstalk-application-maxagerule-deletesourcefroms3): Boolean
[Enabled](#cfn-elasticbeanstalk-application-maxagerule-enabled): Boolean
[MaxAgeInDays](#cfn-elasticbeanstalk-application-maxagerule-maxageindays): Integer
```

## Properties<a name="aws-properties-elasticbeanstalk-application-maxagerule-properties"></a>

`DeleteSourceFromS3`  <a name="cfn-elasticbeanstalk-application-maxagerule-deletesourcefroms3"></a>
Set to `true` to delete a version's source bundle from Amazon S3 when Elastic Beanstalk deletes the application version\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Enabled`  <a name="cfn-elasticbeanstalk-application-maxagerule-enabled"></a>
Specify `true` to apply the rule, or `false` to disable it\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxAgeInDays`  <a name="cfn-elasticbeanstalk-application-maxagerule-maxageindays"></a>
Specify the number of days to retain an application versions\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 