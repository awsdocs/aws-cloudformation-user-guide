# AWS::AppSync::DataSource<a name="aws-resource-appsync-datasource"></a>

The `AWS::AppSync::DataSource` resource creates data sources for resolvers in AWS AppSync to connect to, such as Amazon DynamoDB, AWS Lambda, and Amazon Elasticserach Service\. Resolvers use these data sources to fetch data when clients make GraphQL calls\. 

**Topics**
+ [Syntax](#aws-resource-appsync-datasource-syntax)
+ [Properties](#aws-resource-appsync-datasource-properties)
+ [Return Values](#aws-resource-appsync-datasource-returnvalues)
+ [Examples](#aws-resource-appsync-datasource-examples)
+ [See Also](#aws-resource-appsync-datasource-seealso)

## Syntax<a name="aws-resource-appsync-datasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-datasource-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::DataSource",
  "Properties" : {
    "[Type](#cfn-appsync-datasource-type)" : String,
    "[Description](#cfn-appsync-datasource-description)" : String,
    "[ServiceRoleArn](#cfn-appsync-datasource-servicerolearn)" : String,
    "[LambdaConfig](#cfn-appsync-datasource-lambdaconfig)" : [*LambdaConfig*](aws-properties-appsync-datasource-lambdaconfig.md),
    "[ApiId](#cfn-appsync-datasource-apiid)" : String,
    "[Name](#cfn-appsync-datasource-name)" : String,
    "[DynamoDBConfig](#cfn-appsync-datasource-dynamodbconfig)" : [*DynamoDBConfig*](aws-properties-appsync-datasource-dynamodbconfig.md),
    "[ElasticsearchConfig](#cfn-appsync-datasource-elasticsearchconfig)" : [*ElasticsearchConfig*](aws-properties-appsync-datasource-elasticsearchconfig.md)
  }
}
```

### YAML<a name="aws-resource-appsync-datasource-syntax.yaml"></a>

```
Type: "AWS::AppSync::DataSource"
Properties:
  [Type](#cfn-appsync-datasource-type): String
  [Description](#cfn-appsync-datasource-description): String
  [ServiceRoleArn](#cfn-appsync-datasource-servicerolearn): String
  [LambdaConfig](#cfn-appsync-datasource-lambdaconfig): [*LambdaConfig*](aws-properties-appsync-datasource-lambdaconfig.md)
  [ApiId](#cfn-appsync-datasource-apiid): String
  [Name](#cfn-appsync-datasource-name): String
  [DynamoDBConfig](#cfn-appsync-datasource-dynamodbconfig): [*DynamoDBConfig*](aws-properties-appsync-datasource-dynamodbconfig.md)
  [ElasticsearchConfig](#cfn-appsync-datasource-elasticsearchconfig): [*ElasticsearchConfig*](aws-properties-appsync-datasource-elasticsearchconfig.md)
```

## Properties<a name="aws-resource-appsync-datasource-properties"></a>

`Type`  <a name="cfn-appsync-datasource-type"></a>
Mandatory resource to return data from in customer AWS account\. You can also specify NONE to use Local Resolvers\. See [http://docs.aws.amazon.com/appsync/latest/devguide/tutorial-local-resolvers.html](http://docs.aws.amazon.com/appsync/latest/devguide/tutorial-local-resolvers.html) for more information\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-appsync-datasource-description"></a>
Friendly description for this data source\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceRoleArn`  <a name="cfn-appsync-datasource-servicerolearn"></a>
IAM role ARN which the data source will use to connect to a resource\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaConfig`  <a name="cfn-appsync-datasource-lambdaconfig"></a>
A valid ARN of a Lambda function in your account\.  
 *Required*: No  
 *Type*: [AWS AppSync DataSource LambdaConfig](aws-properties-appsync-datasource-lambdaconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApiId`  <a name="cfn-appsync-datasource-apiid"></a>
Unique AWS AppSync GraphQL API Identifier where this data source will be created\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-appsync-datasource-name"></a>
Friendly name for you to identify your AppSync data source after creation\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DynamoDBConfig`  <a name="cfn-appsync-datasource-dynamodbconfig"></a>
AwsRegion and TableName for an Amazon DynamoDB table in your account\.  
 *Required*: No  
 *Type*: [AWS AppSync DataSource DynamoDBConfig](aws-properties-appsync-datasource-dynamodbconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ElasticsearchConfig`  <a name="cfn-appsync-datasource-elasticsearchconfig"></a>
AwsRegion and Endpoints for an Amazon Elasticsearch Service domain in your account\.  
 *Required*: No  
 *Type*: [AWS AppSync DataSource ElasticsearchConfig](aws-properties-appsync-datasource-elasticsearchconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-appsync-datasource-returnvalues"></a>

### Ref<a name="aws-resource-appsync-datasource-ref"></a>

When you pass the logical ID of an `AWS::AppSync::DataSource` resource to the intrinsic `Ref` function, the function returns the ARN of the Data Source, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/datasources/datasourcename`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-appsync-datasource-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`DataSourceArn`  
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/datasources/datasourcename`\. 

`Name`  
Friendly name for you to identify your AppSync data source after creation\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-appsync-datasource-examples"></a>

### Data Source creation example<a name="aws-resource-appsync-datasource-example1"></a>

The following example creates a data source and associates it with an existing GraphQL API by passing the GraphQL API Id as a paramater\.

#### JSON<a name="aws-resource-appsync-datasource-example1.json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "dataSourceName": {
      "Type": "String"
    },
    "dataSourceDescription": {
      "Type": "String"
    },
    "serviceRoleArn": {
      "Type": "String"
    },
    "lambdaFunctionArn": {
      "Type": "String"
    }
  },
  "Resources": {
    "DataSource": {
      "Type": "AWS::AppSync::DataSource",
      "Properties": {
        "ApiId": {
          "Ref": "graphQlApiId"
        },
        "Name": {
          "Ref": "dataSourceName"
        },
        "Description": {
          "Ref": "dataSourceDescription"
        },
        "Type": "AWS_LAMBDA",
        "ServiceRoleArn": {
           "Ref": "serviceRoleArn"
        },
        "LambdaConfig": {
          "LambdaFunctionArn": {
            "Ref": "lambdaFunctionArn"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appsync-datasource-example1.yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  dataSourceName:
    Type: String
  dataSourceDescription:
    Type: String
  serviceRoleArn:
    Type: String
  lambdaFunctionArn:
    Type: String
Resources:
  DataSource:
    Type: "AWS::AppSync::DataSource"
    Properties:
      ApiId:
        Ref: graphQlApiId
      Name:
        Ref: dataSourceName
      Description:
        Ref: dataSourceDescription
      Type: "AWS_LAMBDA"
      ServiceRoleArn:
        Ref: serviceRoleArn
      LambdaConfig:
        LambdaFunctionArn:
          Ref: lambdaFunctionArn
```

## See Also<a name="aws-resource-appsync-datasource-seealso"></a>
+ [ CreateDataSource](http://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateDataSource.html) operation in the *AWS AppSync API Reference*