# Route 53 QueryLoggingConfig<a name="aws-properties-route53-hostedzone-queryloggingconfig"></a>

The `QueryLoggingConfig` property is part of the [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md) resource that specifies a configuration for DNS query logging\. After you create a query logging configuration, Amazon Route 53 begins to publish log data to an Amazon CloudWatch Logs log group\. For more information, see [CreateQueryLoggingConfig](http://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateQueryLoggingConfig.html) in the *Amazon Route 53 API Reference*\.

## Syntax<a name="w3ab2c21c14e1669b5"></a>

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

## Properties<a name="w3ab2c21c14e1669b7"></a>

`CloudWatchLogsLogGroupArn`  <a name="cfn-route53-hostedzone-queryloggingconfig-cloudwatchlogsloggrouparn"></a>
The Amazon Resource Name \(ARN\) for the log group that you want Amazon Route 53 to send query logs to\. This is the format of the ARN:  
arn:aws:logs:*region:account\-id*:log\-group:*log\_group\_name*  
*Required*: Yes  
*Type*: String