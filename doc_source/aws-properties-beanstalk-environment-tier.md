# Elastic Beanstalk Environment Tier Property Type<a name="aws-properties-beanstalk-environment-tier"></a>

Describes the environment tier for an [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md) resource\. For more information, see [Environment Tiers](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features-managing-env-tiers.html) in the *AWS Elastic Beanstalk Developer Guide*\.

## Syntax<a name="w4ab1c21c14e1042b5"></a>

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

## Members<a name="w4ab1c21c14e1042b7"></a>

`Name`  <a name="cfn-beanstalk-env-tier-name"></a>
The name of the environment tier\. You can specify `WebServer` or `Worker`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Type`  <a name="cfn-beanstalk-env-tier-type"></a>
The type of this environment tier\. You can specify `Standard` for the `WebServer` tier or `SQS/HTTP` for the `Worker` tier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Version`  <a name="cfn-beanstalk-env-tier-version"></a>
The version of this environment tier\. If you don't specify this member, the latest compatible worker tier version is used\.  
This member is deprecated\. Any specific version that you specify may become outdated\. We recommend leaving this unspecified\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)