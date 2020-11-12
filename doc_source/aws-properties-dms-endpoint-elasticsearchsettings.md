# AWS::DMS::Endpoint ElasticsearchSettings<a name="aws-properties-dms-endpoint-elasticsearchsettings"></a>

Provides information that defines an Elasticsearch endpoint\.

## Syntax<a name="aws-properties-dms-endpoint-elasticsearchsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-elasticsearchsettings-syntax.json"></a>

```
{
  "[EndpointUri](#cfn-dms-endpoint-elasticsearchsettings-endpointuri)" : String,
  "[ErrorRetryDuration](#cfn-dms-endpoint-elasticsearchsettings-errorretryduration)" : Integer,
  "[FullLoadErrorPercentage](#cfn-dms-endpoint-elasticsearchsettings-fullloaderrorpercentage)" : Integer,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-elasticsearchsettings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-elasticsearchsettings-syntax.yaml"></a>

```
  [EndpointUri](#cfn-dms-endpoint-elasticsearchsettings-endpointuri): String
  [ErrorRetryDuration](#cfn-dms-endpoint-elasticsearchsettings-errorretryduration): Integer
  [FullLoadErrorPercentage](#cfn-dms-endpoint-elasticsearchsettings-fullloaderrorpercentage): Integer
  [ServiceAccessRoleArn](#cfn-dms-endpoint-elasticsearchsettings-serviceaccessrolearn): String
```

## Properties<a name="aws-properties-dms-endpoint-elasticsearchsettings-properties"></a>

`EndpointUri`  <a name="cfn-dms-endpoint-elasticsearchsettings-endpointuri"></a>
The endpoint for the Elasticsearch cluster\. AWS DMS uses HTTPS if a transport protocol \(http/https\) is not specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorRetryDuration`  <a name="cfn-dms-endpoint-elasticsearchsettings-errorretryduration"></a>
The maximum number of seconds for which DMS retries failed API requests to the Elasticsearch cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullLoadErrorPercentage`  <a name="cfn-dms-endpoint-elasticsearchsettings-fullloaderrorpercentage"></a>
The maximum percentage of records that can fail to be written before a full load operation stops\.  
To avoid early failure, this counter is only effective after 1000 records are transferred\. Elasticsearch also has the concept of error monitoring during the last 10 minutes of an Observation Window\. If transfer of all records fail in the last 10 minutes, the full load operation stops\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-elasticsearchsettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) used by service to access the IAM role\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)