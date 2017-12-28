# AWS Elastic Beanstalk Application ApplicationResourceLifecycleConfig<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig"></a>

<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-description"></a>The `ApplicationResourceLifecycleConfig` property type specifies lifecycle settings for resources that belong to the application, and the service role that AWS Elastic Beanstalk assumes in order to apply lifecycle settings\.

<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-inheritance"></a> `ApplicationResourceLifecycleConfig` is a property of the [AWS::ElasticBeanstalk::Application](aws-properties-beanstalk.md) resource\. 

## Syntax<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-servicerole)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-versionlifecycleconfig)" : ApplicationVersionLifecycleConfig
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-servicerole): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-applicationresourcelifecycleconfig-versionlifecycleconfig):
  ApplicationVersionLifecycleConfig
```

## Properties<a name="aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig-properties"></a>

`ServiceRole`  
The ARN of an IAM service role that Elastic Beanstalk has permission to assume\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`VersionLifecycleConfig`  
Defines lifecycle settings for application versions\.  
 *Required*: No  
 *Type*: [Elastic Beanstalk Application ApplicationVersionLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.md)  
 *Update requires*: No interruption 