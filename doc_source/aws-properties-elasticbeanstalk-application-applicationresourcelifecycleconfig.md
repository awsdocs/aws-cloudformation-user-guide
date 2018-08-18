# AWS Elastic Beanstalk Application ApplicationResourceLifecycleConfig<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig"></a>

<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-description"></a>The `ApplicationResourceLifecycleConfig` property type specifies lifecycle settings for resources that belong to the application, and the service role that AWS Elastic Beanstalk assumes in order to apply lifecycle settings\.

<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-inheritance"></a> `ApplicationResourceLifecycleConfig` is a property of the [AWS::ElasticBeanstalk::Application](aws-properties-beanstalk.md) resource\. 

## Syntax<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax.json"></a>

```
{
  "[ServiceRole](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-servicerole)" : String,
  "[VersionLifecycleConfig](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-versionlifecycleconfig)" : [*ApplicationVersionLifecycleConfig*](aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.md)
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax.yaml"></a>

```
[ServiceRole](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-servicerole): String
[VersionLifecycleConfig](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-versionlifecycleconfig):
  ApplicationVersionLifecycleConfig
```

## Properties<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-properties"></a>

`ServiceRole`  <a name="cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-servicerole"></a>
The ARN of an IAM service role that Elastic Beanstalk has permission to assume\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VersionLifecycleConfig`  <a name="cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-versionlifecycleconfig"></a>
Defines lifecycle settings for application versions\.  
 *Required*: No  
 *Type*: [Elastic Beanstalk Application ApplicationVersionLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 