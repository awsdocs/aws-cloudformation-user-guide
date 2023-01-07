# AWS::Route53::HostedZone QueryLoggingConfig<a name="aws-properties-route53-hostedzone-queryloggingconfig"></a>

A complex type that contains information about a configuration for DNS query logging\.

## Syntax<a name="aws-properties-route53-hostedzone-queryloggingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-hostedzone-queryloggingconfig-syntax.json"></a>

```
{
  "[CloudWatchLogsLogGroupArn](#cfn-route53-hostedzone-queryloggingconfig-cloudwatchlogsloggrouparn)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-queryloggingconfig-syntax.yaml"></a>

```
  [CloudWatchLogsLogGroupArn](#cfn-route53-hostedzone-queryloggingconfig-cloudwatchlogsloggrouparn): String
```

## Properties<a name="aws-properties-route53-hostedzone-queryloggingconfig-properties"></a>

`CloudWatchLogsLogGroupArn`  <a name="cfn-route53-hostedzone-queryloggingconfig-cloudwatchlogsloggrouparn"></a>
The Amazon Resource Name \(ARN\) of the CloudWatch Logs log group that Amazon Route 53 is publishing logs to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-hostedzone-queryloggingconfig--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html#aws-resource-route53-hostedzone-return-values) in the topic [AWS::Route53::HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html) 
+  [QueryLoggingConfig](https://docs.aws.amazon.com/Route53/latest/APIReference/API_QueryLoggingConfig.html) in the *Amazon Route 53 API Reference*

