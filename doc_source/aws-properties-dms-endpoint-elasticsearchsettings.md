# AWS::DMS::Endpoint ElasticsearchSettings<a name="aws-properties-dms-endpoint-elasticsearchsettings"></a>

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
The endpoint for the ElasticSearch cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorRetryDuration`  <a name="cfn-dms-endpoint-elasticsearchsettings-errorretryduration"></a>
The maximum number of seconds that DMS retries failed API requests to the Elasticsearch cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullLoadErrorPercentage`  <a name="cfn-dms-endpoint-elasticsearchsettings-fullloaderrorpercentage"></a>
The maximum percentage of records that can fail to be written before a full load operation stops\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-elasticsearchsettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) used by service to access the IAM role\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
