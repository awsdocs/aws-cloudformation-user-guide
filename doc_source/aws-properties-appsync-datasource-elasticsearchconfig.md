# AWS::AppSync::DataSource ElasticsearchConfig<a name="aws-properties-appsync-datasource-elasticsearchconfig"></a>

The `ElasticsearchConfig` property type specifies the `AwsRegion` and `Endpoints` for an Amazon Elasticsearch Service domain in your account for an AWS AppSync data source\.

ElasticsearchConfig is a property of the [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html) property type\. 

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
The AWS Region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-appsync-datasource-elasticsearchconfig-endpoint"></a>
The endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)