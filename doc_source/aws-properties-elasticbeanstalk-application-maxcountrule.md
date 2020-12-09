# AWS::ElasticBeanstalk::Application MaxCountRule<a name="aws-properties-elasticbeanstalk-application-maxcountrule"></a>

A lifecycle rule that deletes the oldest application version when the maximum count is exceeded\.

 `MaxCountRule` is a property of the [ApplicationVersionLifecycleConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticbeanstalk-application-applicationversionlifecycleconfig.html) property type\.

## Syntax<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax.json"></a>

```
{
  "[DeleteSourceFromS3](#cfn-elasticbeanstalk-application-maxcountrule-deletesourcefroms3)" : Boolean,
  "[Enabled](#cfn-elasticbeanstalk-application-maxcountrule-enabled)" : Boolean,
  "[MaxCount](#cfn-elasticbeanstalk-application-maxcountrule-maxcount)" : Integer
}
```

### YAML<a name="aws-properties-elasticbeanstalk-application-maxcountrule-syntax.yaml"></a>

```
  [DeleteSourceFromS3](#cfn-elasticbeanstalk-application-maxcountrule-deletesourcefroms3): Boolean
  [Enabled](#cfn-elasticbeanstalk-application-maxcountrule-enabled): Boolean
  [MaxCount](#cfn-elasticbeanstalk-application-maxcountrule-maxcount): Integer
```

## Properties<a name="aws-properties-elasticbeanstalk-application-maxcountrule-properties"></a>

`DeleteSourceFromS3`  <a name="cfn-elasticbeanstalk-application-maxcountrule-deletesourcefroms3"></a>
Set to `true` to delete a version's source bundle from Amazon S3 when Elastic Beanstalk deletes the application version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-elasticbeanstalk-application-maxcountrule-enabled"></a>
Specify `true` to apply the rule, or `false` to disable it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCount`  <a name="cfn-elasticbeanstalk-application-maxcountrule-maxcount"></a>
Specify the maximum number of application versions to retain\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)