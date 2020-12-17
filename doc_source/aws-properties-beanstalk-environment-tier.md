# AWS::ElasticBeanstalk::Environment Tier<a name="aws-properties-beanstalk-environment-tier"></a>

Describes the environment tier for an [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html) resource\. For more information, see [Environment Tiers](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features-managing-env-tiers.html) in the *AWS Elastic Beanstalk Developer Guide*\.

## Syntax<a name="aws-properties-beanstalk-environment-tier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-environment-tier-syntax.json"></a>

```
{
  "[Name](#cfn-beanstalk-env-tier-name)" : String,
  "[Type](#cfn-beanstalk-env-tier-type)" : String,
  "[Version](#cfn-beanstalk-env-tier-version)" : String
}
```

### YAML<a name="aws-properties-beanstalk-environment-tier-syntax.yaml"></a>

```
  [Name](#cfn-beanstalk-env-tier-name): String
  [Type](#cfn-beanstalk-env-tier-type): String
  [Version](#cfn-beanstalk-env-tier-version): String
```

## Properties<a name="aws-properties-beanstalk-environment-tier-properties"></a>

`Name`  <a name="cfn-beanstalk-env-tier-name"></a>
The name of this environment tier\.  
Valid values:  
+ For *Web server tier* – `WebServer` 
+ For *Worker tier* – `Worker` 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-beanstalk-env-tier-type"></a>
The type of this environment tier\.  
Valid values:  
+ For *Web server tier* – `Standard` 
+ For *Worker tier* – `SQS/HTTP` 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-beanstalk-env-tier-version"></a>
The version of this environment tier\. When you don't set a value to it, Elastic Beanstalk uses the latest compatible worker tier version\.  
This member is deprecated\. Any specific version that you set may become out of date\. We recommend leaving it unspecified\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)