# AWS::Elasticsearch::Domain LogPublishingOption<a name="aws-properties-elasticsearch-domain-logpublishingoption"></a>

Specifies whether the Amazon ES domain publishes the Elasticsearch application, search slow logs, or index slow logs to Amazon CloudWatch\. Each option must be an object of name `SEARCH_SLOW_LOGS`, `ES_APPLICATION_LOGS`, `INDEX_SLOW_LOGS`, or `AUDIT_LOGS` depending on the type of logs you want to publish\. See [here](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html#aws-resource-elasticsearch-domain--examples) for the full syntax\.

If you enable a slow log, you still have to enable the *collection* of slow logs using the Elasticsearch REST API\. To learn more, see [Setting Elasticsearch Logging Thresholds for Slow Logs](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-slow-logs-indices)\.

## Syntax<a name="aws-properties-elasticsearch-domain-logpublishingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-logpublishingoption-syntax.json"></a>

```
{
  "[CloudWatchLogsLogGroupArn](#cfn-elasticsearch-domain-logpublishingoption-cloudwatchlogsloggrouparn)" : String,
  "[Enabled](#cfn-elasticsearch-domain-logpublishingoption-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-logpublishingoption-syntax.yaml"></a>

```
  [CloudWatchLogsLogGroupArn](#cfn-elasticsearch-domain-logpublishingoption-cloudwatchlogsloggrouparn): String
  [Enabled](#cfn-elasticsearch-domain-logpublishingoption-enabled): Boolean
```

## Properties<a name="aws-properties-elasticsearch-domain-logpublishingoption-properties"></a>

`CloudWatchLogsLogGroupArn`  <a name="cfn-elasticsearch-domain-logpublishingoption-cloudwatchlogsloggrouparn"></a>
Specifies the CloudWatch log group to publish to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-elasticsearch-domain-logpublishingoption-enabled"></a>
If `true`, enables the publishing of logs to CloudWatch\.  
Default: `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-elasticsearch-domain-logpublishingoption--seealso"></a>
+ [Configuring Logs](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-slow-logs) and [Log Publishing Options](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-datatypes-logpublishingoptions) in the *Amazon Elasticsearch Service Developer Guide*\.

