# AWS::Route53::HealthCheck AlarmIdentifier<a name="aws-properties-route53-healthcheck-alarmidentifier"></a>

A complex type that identifies the CloudWatch alarm that you want Amazon Route 53 health checkers to use to determine whether the specified health check is healthy\.

## Syntax<a name="aws-properties-route53-healthcheck-alarmidentifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-healthcheck-alarmidentifier-syntax.json"></a>

```
{
  "[Name](#cfn-route53-healthcheck-alarmidentifier-name)" : String,
  "[Region](#cfn-route53-healthcheck-alarmidentifier-region)" : String
}
```

### YAML<a name="aws-properties-route53-healthcheck-alarmidentifier-syntax.yaml"></a>

```
  [Name](#cfn-route53-healthcheck-alarmidentifier-name): String
  [Region](#cfn-route53-healthcheck-alarmidentifier-region): String
```

## Properties<a name="aws-properties-route53-healthcheck-alarmidentifier-properties"></a>

`Name`  <a name="cfn-route53-healthcheck-alarmidentifier-name"></a>
The name of the CloudWatch alarm that you want Amazon Route 53 health checkers to use to determine whether this health check is healthy\.  
Route 53 supports CloudWatch alarms with the following features:  
+ Standard\-resolution metrics\. High\-resolution metrics aren't supported\. For more information, see [High\-Resolution Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/publishingMetrics.html#high-resolution-metrics) in the *Amazon CloudWatch User Guide*\.
+ Statistics: Average, Minimum, Maximum, Sum, and SampleCount\. Extended statistics aren't supported\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-route53-healthcheck-alarmidentifier-region"></a>
For the CloudWatch alarm that you want Route 53 health checkers to use to determine whether this health check is healthy, the region that the alarm was created in\.  
For the current list of CloudWatch regions, see [Amazon CloudWatch endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/cw_region.html) in the *Amazon Web Services General Reference*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `af-south-1 | ap-east-1 | ap-northeast-1 | ap-northeast-2 | ap-northeast-3 | ap-south-1 | ap-southeast-1 | ap-southeast-2 | ap-southeast-3 | ca-central-1 | cn-north-1 | cn-northwest-1 | eu-central-1 | eu-north-1 | eu-south-1 | eu-west-1 | eu-west-2 | eu-west-3 | me-south-1 | sa-east-1 | us-east-1 | us-east-2 | us-gov-east-1 | us-gov-west-1 | us-iso-east-1 | us-iso-west-1 | us-isob-east-1 | us-west-1 | us-west-2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-healthcheck-alarmidentifier--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-healthcheck.html#aws-resource-route53-healthcheck-return-values) in the topic [AWS::Route53::HealthCheck](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-healthcheck.html) 
+  [AlarmIdentifier](https://docs.aws.amazon.com/Route53/latest/APIReference/API_AlarmIdentifier.html) in the *Amazon Route 53 API Reference* 

