# AWS Elastic Beanstalk Application MaxCountRule<a name="aws-properties-elasticbeanstalk-application-maxcountrule"></a>

<a name="aws-properties-elasticbeanstalk-application-maxcountrule-description"></a>The `MaxCountRule` property type specifies a lifecycle rule that deletes the oldest application version when the maximum count is exceeded for an AWS Elastic Beanstalk application\.

<a name="aws-properties-elasticbeanstalk-application-maxcountrule-inheritance"></a> `MaxCountRule` is a property of the [Elastic Beanstalk Application ApplicationVersionLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.md) property type\. 

## Syntax<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-deletesourcefroms3)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-maxcount)" : Integer
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-deletesourcefroms3): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-maxcountrule-maxcount): Integer
```

## Properties<a name="aws-properties-elasticbeanstalk-application-maxcountrule-properties"></a>

`DeleteSourceFromS3`  
Set to `true` to delete a version's source bundle from Amazon S3 when Elastic Beanstalk deletes the application version\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Enabled`  
Specify `true` to apply the rule, or `false` to disable it\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`MaxCount`  
Specify the maximum number of application versions to retain\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 