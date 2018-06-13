# AWS AppSync DataSource ElasticsearchConfig<a name="aws-properties-appsync-datasource-elasticsearchconfig"></a>

<a name="aws-properties-appsync-datasource-elasticsearchconfig-description"></a>The `ElasticsearchConfig` property type specifies the AwsRegion and Endpoints for an Amazon Elasticsearch Service domain in your account for an AWS AppSync data source\.

<a name="aws-properties-appsync-datasource-elasticsearchconfig-inheritance"></a> `ElasticsearchConfig` is a property of the [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md) property type\.

## Syntax<a name="aws-properties-appsync-datasource-elasticsearchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-elasticsearchconfig-syntax.json"></a>

```
{
  "[AwsRegion](#cfn-appsync-datasource-elasticsearchconfig-awsregion)" : String,
  "[Endpoint](#cfn-appsync-datasource-elasticsearchconfig-endpoint)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-elasticsearchconfig-syntax.yaml"></a>

```
[AwsRegion](#cfn-appsync-datasource-elasticsearchconfig-awsregion): String
[Endpoint](#cfn-appsync-datasource-elasticsearchconfig-endpoint): String
```

## Properties<a name="aws-properties-appsync-datasource-elasticsearchconfig-properties"></a>

`AwsRegion`  <a name="cfn-appsync-datasource-elasticsearchconfig-awsregion"></a>
The AWS region\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Endpoint`  <a name="cfn-appsync-datasource-elasticsearchconfig-endpoint"></a>
The endpoint\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-elasticsearchconfig-seealso"></a>
+ [ ElasticsearchDataSourceConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_ElasticsearchDataSourceConfig.html) operation in the *AWS AppSync API Reference*