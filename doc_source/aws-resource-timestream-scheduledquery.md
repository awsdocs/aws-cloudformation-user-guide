# AWS::Timestream::ScheduledQuery<a name="aws-resource-timestream-scheduledquery"></a>

 Create a scheduled query that will be run on your behalf at the configured schedule\. Timestream assumes the execution role provided as part of the `ScheduledQueryExecutionRoleArn` parameter to run the query\. You can use the `NotificationConfiguration` parameter to configure notification for your scheduled query operations\.

## Syntax<a name="aws-resource-timestream-scheduledquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-timestream-scheduledquery-syntax.json"></a>

```
{
  "Type" : "AWS::Timestream::ScheduledQuery",
  "Properties" : {
      "[ClientToken](#cfn-timestream-scheduledquery-clienttoken)" : String,
      "[ErrorReportConfiguration](#cfn-timestream-scheduledquery-errorreportconfiguration)" : ErrorReportConfiguration,
      "[KmsKeyId](#cfn-timestream-scheduledquery-kmskeyid)" : String,
      "[NotificationConfiguration](#cfn-timestream-scheduledquery-notificationconfiguration)" : NotificationConfiguration,
      "[QueryString](#cfn-timestream-scheduledquery-querystring)" : String,
      "[ScheduleConfiguration](#cfn-timestream-scheduledquery-scheduleconfiguration)" : ScheduleConfiguration,
      "[ScheduledQueryExecutionRoleArn](#cfn-timestream-scheduledquery-scheduledqueryexecutionrolearn)" : String,
      "[ScheduledQueryName](#cfn-timestream-scheduledquery-scheduledqueryname)" : String,
      "[Tags](#cfn-timestream-scheduledquery-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetConfiguration](#cfn-timestream-scheduledquery-targetconfiguration)" : TargetConfiguration
    }
}
```

### YAML<a name="aws-resource-timestream-scheduledquery-syntax.yaml"></a>

```
Type: AWS::Timestream::ScheduledQuery
Properties: 
  [ClientToken](#cfn-timestream-scheduledquery-clienttoken): String
  [ErrorReportConfiguration](#cfn-timestream-scheduledquery-errorreportconfiguration): 
    ErrorReportConfiguration
  [KmsKeyId](#cfn-timestream-scheduledquery-kmskeyid): String
  [NotificationConfiguration](#cfn-timestream-scheduledquery-notificationconfiguration): 
    NotificationConfiguration
  [QueryString](#cfn-timestream-scheduledquery-querystring): 
    String
  [ScheduleConfiguration](#cfn-timestream-scheduledquery-scheduleconfiguration): 
    ScheduleConfiguration
  [ScheduledQueryExecutionRoleArn](#cfn-timestream-scheduledquery-scheduledqueryexecutionrolearn): String
  [ScheduledQueryName](#cfn-timestream-scheduledquery-scheduledqueryname): String
  [Tags](#cfn-timestream-scheduledquery-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetConfiguration](#cfn-timestream-scheduledquery-targetconfiguration): 
    TargetConfiguration
```

## Properties<a name="aws-resource-timestream-scheduledquery-properties"></a>

`ClientToken`  <a name="cfn-timestream-scheduledquery-clienttoken"></a>
Using a ClientToken makes the call to CreateScheduledQuery idempotent, in other words, making the same request repeatedly will produce the same result\. Making multiple identical CreateScheduledQuery requests has the same effect as making a single request\.   
+  If CreateScheduledQuery is called without a `ClientToken`, the Query SDK generates a `ClientToken` on your behalf\.
+  After 8 hours, any request with the same `ClientToken` is treated as a new request\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ErrorReportConfiguration`  <a name="cfn-timestream-scheduledquery-errorreportconfiguration"></a>
Configuration for error reporting\. Error reports will be generated when a problem is encountered when writing the query results\.   
*Required*: Yes  
*Type*: [ErrorReportConfiguration](aws-properties-timestream-scheduledquery-errorreportconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-timestream-scheduledquery-kmskeyid"></a>
The Amazon KMS key used to encrypt the scheduled query resource, at\-rest\. If the Amazon KMS key is not specified, the scheduled query resource will be encrypted with a Timestream owned Amazon KMS key\. To specify a KMS key, use the key ID, key ARN, alias name, or alias ARN\. When using an alias name, prefix the name with *alias/*  
If ErrorReportConfiguration uses `SSE_KMS` as encryption type, the same KmsKeyId is used to encrypt the error report at rest\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotificationConfiguration`  <a name="cfn-timestream-scheduledquery-notificationconfiguration"></a>
Notification configuration for the scheduled query\. A notification is sent by Timestream when a query run finishes, when the state is updated or when you delete it\.   
*Required*: Yes  
*Type*: [NotificationConfiguration](aws-properties-timestream-scheduledquery-notificationconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QueryString`  <a name="cfn-timestream-scheduledquery-querystring"></a>
The query string to run\. Parameter names can be specified in the query string `@` character followed by an identifier\. The named Parameter `@scheduled_runtime` is reserved and can be used in the query to get the time at which the query is scheduled to run\.  
The timestamp calculated according to the ScheduleConfiguration parameter, will be the value of `@scheduled_runtime` paramater for each query run\. For example, consider an instance of a scheduled query executing on 2021\-12\-01 00:00:00\. For this instance, the `@scheduled_runtime` parameter is initialized to the timestamp 2021\-12\-01 00:00:00 when invoking the query\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduleConfiguration`  <a name="cfn-timestream-scheduledquery-scheduleconfiguration"></a>
Schedule configuration\.  
*Required*: Yes  
*Type*: [ScheduleConfiguration](aws-properties-timestream-scheduledquery-scheduleconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduledQueryExecutionRoleArn`  <a name="cfn-timestream-scheduledquery-scheduledqueryexecutionrolearn"></a>
The ARN for the IAM role that Timestream will assume when running the scheduled query\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduledQueryName`  <a name="cfn-timestream-scheduledquery-scheduledqueryname"></a>
A name for the query\. Scheduled query names must be unique within each Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-timestream-scheduledquery-tags"></a>
A list of key\-value pairs to label the scheduled query\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetConfiguration`  <a name="cfn-timestream-scheduledquery-targetconfiguration"></a>
Scheduled query target store configuration\.  
*Required*: No  
*Type*: [TargetConfiguration](aws-properties-timestream-scheduledquery-targetconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-timestream-scheduledquery-return-values"></a>

### Ref<a name="aws-resource-timestream-scheduledquery-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the scheduled query ARN\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-timestream-scheduledquery-return-values-fn--getatt"></a>

The `Fn::GetAtt` returns a value for the specified attribute of this type\. The following are the available attributes:

#### <a name="aws-resource-timestream-scheduledquery-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The `ARN` of the scheduled query\.

`SQErrorReportConfiguration`  <a name="SQErrorReportConfiguration-fn::getatt"></a>
The scheduled query error reporting configuration\.

`SQKmsKeyId`  <a name="SQKmsKeyId-fn::getatt"></a>
The KMS key used to encrypt the query resource, if a customer managed KMS key was provided\.

`SQName`  <a name="SQName-fn::getatt"></a>
The scheduled query name\.

`SQNotificationConfiguration`  <a name="SQNotificationConfiguration-fn::getatt"></a>
The scheduled query notification configuration\.

`SQQueryString`  <a name="SQQueryString-fn::getatt"></a>
The scheduled query string\.\.

`SQScheduleConfiguration`  <a name="SQScheduleConfiguration-fn::getatt"></a>
The scheduled query schedule configuration\.

`SQScheduledQueryExecutionRoleArn`  <a name="SQScheduledQueryExecutionRoleArn-fn::getatt"></a>
The ARN of the IAM role that will be used by Timestream to run the query\.

`SQTargetConfiguration`  <a name="SQTargetConfiguration-fn::getatt"></a>
The configuration for query output\.