# AWS::CloudWatch::MetricStream<a name="aws-resource-cloudwatch-metricstream"></a>

Creates or updates a metric stream\. Metrics streams can automatically stream CloudWatch metrics to AWS destinations including Amazon S3 and to many third\-party solutions\. For more information, see [ Metric streams](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Metric-Streams.html)\. 

To create a metric stream, you must be logged on to an account that has the `iam:PassRole` permission and either the **CloudWatchFullAccess** policy or the `cloudwatch:PutMetricStream` permission\. 

When you create or update a metric stream, you choose one of the following:
+ Stream metrics from all metric namespaces in the account\.
+ Stream metrics from all metric namespaces in the account, except for the namespaces that you list in `ExcludeFilters`\.
+ Stream metrics from only the metric namespaces that you list in `IncludeFilters`\. 

When you create a metric stream, the stream is created in the `running` state\. If you update an existing metric stream, the state does not change\.

If you create a metric stream in an account that has been set up as a monitoring account in CloudWatch cross\-account observability, you can choose whether to include metrics from linked source accounts in the metric stream\.

## Syntax<a name="aws-resource-cloudwatch-metricstream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudwatch-metricstream-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::MetricStream",
  "Properties" : {
      "[ExcludeFilters](#cfn-cloudwatch-metricstream-excludefilters)" : [ MetricStreamFilter, ... ],
      "[FirehoseArn](#cfn-cloudwatch-metricstream-firehosearn)" : String,
      "[IncludeFilters](#cfn-cloudwatch-metricstream-includefilters)" : [ MetricStreamFilter, ... ],
      "[IncludeLinkedAccountsMetrics](#cfn-cloudwatch-metricstream-includelinkedaccountsmetrics)" : Boolean,
      "[Name](#cfn-cloudwatch-metricstream-name)" : String,
      "[OutputFormat](#cfn-cloudwatch-metricstream-outputformat)" : String,
      "[RoleArn](#cfn-cloudwatch-metricstream-rolearn)" : String,
      "[StatisticsConfigurations](#cfn-cloudwatch-metricstream-statisticsconfigurations)" : [ MetricStreamStatisticsConfiguration, ... ],
      "[Tags](#cfn-cloudwatch-metricstream-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cloudwatch-metricstream-syntax.yaml"></a>

```
Type: AWS::CloudWatch::MetricStream
Properties: 
  [ExcludeFilters](#cfn-cloudwatch-metricstream-excludefilters): 
    - MetricStreamFilter
  [FirehoseArn](#cfn-cloudwatch-metricstream-firehosearn): String
  [IncludeFilters](#cfn-cloudwatch-metricstream-includefilters): 
    - MetricStreamFilter
  [IncludeLinkedAccountsMetrics](#cfn-cloudwatch-metricstream-includelinkedaccountsmetrics): Boolean
  [Name](#cfn-cloudwatch-metricstream-name): String
  [OutputFormat](#cfn-cloudwatch-metricstream-outputformat): String
  [RoleArn](#cfn-cloudwatch-metricstream-rolearn): String
  [StatisticsConfigurations](#cfn-cloudwatch-metricstream-statisticsconfigurations): 
    - MetricStreamStatisticsConfiguration
  [Tags](#cfn-cloudwatch-metricstream-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cloudwatch-metricstream-properties"></a>

`ExcludeFilters`  <a name="cfn-cloudwatch-metricstream-excludefilters"></a>
If you specify this parameter, the stream sends metrics from all metric namespaces except for the namespaces that you specify here\. You cannot specify both `IncludeFilters` and `ExcludeFilters` in the same metric stream\.  
When you modify the `IncludeFilters` or `ExcludeFilters` of an existing metric stream in any way, the metric stream is effectively restarted, so after such a change you will get only the datapoints that have a timestamp after the time of the update\.  
*Required*: No  
*Type*: List of [MetricStreamFilter](aws-properties-cloudwatch-metricstream-metricstreamfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirehoseArn`  <a name="cfn-cloudwatch-metricstream-firehosearn"></a>
The ARN of the Amazon Kinesis Firehose delivery stream to use for this metric stream\. This Amazon Kinesis Firehose delivery stream must already exist and must be in the same account as the metric stream\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeFilters`  <a name="cfn-cloudwatch-metricstream-includefilters"></a>
If you specify this parameter, the stream sends only the metrics from the metric namespaces that you specify here\. You cannot specify both `IncludeFilters` and `ExcludeFilters` in the same metric stream\.  
When you modify the `IncludeFilters` or `ExcludeFilters` of an existing metric stream in any way, the metric stream is effectively restarted, so after such a change you will get only the datapoints that have a timestamp after the time of the update\.  
*Required*: No  
*Type*: List of [MetricStreamFilter](aws-properties-cloudwatch-metricstream-metricstreamfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeLinkedAccountsMetrics`  <a name="cfn-cloudwatch-metricstream-includelinkedaccountsmetrics"></a>
If you are creating a metric stream in a monitoring account, specify `true` to include metrics from source accounts that are linked to this monitoring account, in the metric stream\. The default is `false`\.  
For more information about linking accounts, see [CloudWatch cross\-account observability](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Unified-Cross-Account.html)   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudwatch-metricstream-name"></a>
If you are creating a new metric stream, this is the name for the new stream\. The name must be different than the names of other metric streams in this account and Region\.  
If you are updating a metric stream, specify the name of that stream here\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutputFormat`  <a name="cfn-cloudwatch-metricstream-outputformat"></a>
The output format for the stream\. Valid values are `json` and `opentelemetry0.7` For more information about metric stream output formats, see [ Metric streams output formats](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-metric-streams-formats.html)\.  
This parameter is required\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-cloudwatch-metricstream-rolearn"></a>
The ARN of an IAM role that this metric stream will use to access Amazon Kinesis Firehose resources\. This IAM role must already exist and must be in the same account as the metric stream\. This IAM role must include the `firehose:PutRecord` and `firehose:PutRecordBatch` permissions\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatisticsConfigurations`  <a name="cfn-cloudwatch-metricstream-statisticsconfigurations"></a>
By default, a metric stream always sends the MAX, MIN, SUM, and SAMPLECOUNT statistics for each metric that is streamed\. You can use this parameter to have the metric stream also send additional statistics in the stream\. This array can have up to 100 members\.  
For each entry in this array, you specify one or more metrics and the list of additional statistics to stream for those metrics\. The additional statistics that you can stream depend on the stream's `OutputFormat`\. If the `OutputFormat` is `json`, you can stream any additional statistic that is supported by CloudWatch, listed in [CloudWatch statistics definitions](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Statistics-definitions.html.html)\. If the `OutputFormat` is `opentelemetry0`\.7, you can stream percentile statistics *\(p??\)*\.  
*Required*: No  
*Type*: List of [MetricStreamStatisticsConfiguration](aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudwatch-metricstream-tags"></a>
An array of key\-value pairs to apply to the metric stream\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudwatch-metricstream-return-values"></a>

### Ref<a name="aws-resource-cloudwatch-metricstream-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the metric stream\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudwatch-metricstream-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudwatch-metricstream-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the metric stream\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The date that the metric stream was originally created\.

`LastUpdateDate`  <a name="LastUpdateDate-fn::getatt"></a>
The date that the metric stream was most recently updated\.

`State`  <a name="State-fn::getatt"></a>
The state of the metric stream, either `running` or `stopped`\.

## Examples<a name="aws-resource-cloudwatch-metricstream--examples"></a>

### Metric stream example<a name="aws-resource-cloudwatch-metricstream--examples--Metric_stream_example"></a>

The following example creates a metric stream that streams only the metrics in the `AWS/ELB` and `AWS/EC2` namespaces\.

#### YAML<a name="aws-resource-cloudwatch-metricstream--examples--Metric_stream_example--yaml"></a>

```
Resources:
  MyMetricStream:
    Type: 'AWS::CloudWatch::MetricStream'
    Properties:
      OutputFormat: 'json'
      FirehoseArn: 'arn:aws:firehose:us-east-1:123456789012:deliverystream/MyDeliveryStream'
      RoleArn: 'arn:aws:iam::123456789012:role/service-role/MyRole'
      IncludeFilters:
        - Namespace: AWS/ELB
        - Namespace: AWS/EC2
```

#### JSON<a name="aws-resource-cloudwatch-metricstream--examples--Metric_stream_example--json"></a>

```
{
  "Type" : "AWS::CloudWatch::MetricStream",
  "Properties" : {
    "FirehoseArn" : "arn:aws:firehose:us-east-1:123456789012:deliverystream/MyDeliveryStream",
    "IncludeFilters" : [
      {
        "Namespace": "AWS/ELB"
      },
      {
        "Namespace": "AWS/EC2"
      }
    ],
    "Name" : "MyMetricStream",
    "OutputFormat" : "json",
    "RoleArn" : "arn:aws:iam::123456789012:role/service-role/MyRole"
  }
}
```