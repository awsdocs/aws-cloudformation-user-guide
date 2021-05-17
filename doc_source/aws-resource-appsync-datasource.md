# AWS::AppSync::DataSource<a name="aws-resource-appsync-datasource"></a>

The `AWS::AppSync::DataSource` resource creates data sources for resolvers in AWS AppSync to connect to, such as Amazon DynamoDB, AWS Lambda, and Amazon Elasticsearch Service\. Resolvers use these data sources to fetch data when clients make GraphQL calls\. 

## Syntax<a name="aws-resource-appsync-datasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-datasource-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::DataSource",
  "Properties" : {
      "[ApiId](#cfn-appsync-datasource-apiid)" : String,
      "[Description](#cfn-appsync-datasource-description)" : String,
      "[DynamoDBConfig](#cfn-appsync-datasource-dynamodbconfig)" : DynamoDBConfig,
      "[ElasticsearchConfig](#cfn-appsync-datasource-elasticsearchconfig)" : ElasticsearchConfig,
      "[HttpConfig](#cfn-appsync-datasource-httpconfig)" : HttpConfig,
      "[LambdaConfig](#cfn-appsync-datasource-lambdaconfig)" : LambdaConfig,
      "[Name](#cfn-appsync-datasource-name)" : String,
      "[RelationalDatabaseConfig](#cfn-appsync-datasource-relationaldatabaseconfig)" : RelationalDatabaseConfig,
      "[ServiceRoleArn](#cfn-appsync-datasource-servicerolearn)" : String,
      "[Type](#cfn-appsync-datasource-type)" : String
    }
}
```

### YAML<a name="aws-resource-appsync-datasource-syntax.yaml"></a>

```
Type: AWS::AppSync::DataSource
Properties: 
  [ApiId](#cfn-appsync-datasource-apiid): String
  [Description](#cfn-appsync-datasource-description): String
  [DynamoDBConfig](#cfn-appsync-datasource-dynamodbconfig): 
    DynamoDBConfig
  [ElasticsearchConfig](#cfn-appsync-datasource-elasticsearchconfig): 
    ElasticsearchConfig
  [HttpConfig](#cfn-appsync-datasource-httpconfig): 
    HttpConfig
  [LambdaConfig](#cfn-appsync-datasource-lambdaconfig): 
    LambdaConfig
  [Name](#cfn-appsync-datasource-name): String
  [RelationalDatabaseConfig](#cfn-appsync-datasource-relationaldatabaseconfig): 
    RelationalDatabaseConfig
  [ServiceRoleArn](#cfn-appsync-datasource-servicerolearn): String
  [Type](#cfn-appsync-datasource-type): String
```

## Properties<a name="aws-resource-appsync-datasource-properties"></a>

`ApiId`  <a name="cfn-appsync-datasource-apiid"></a>
Unique AWS AppSync GraphQL API identifier where this data source will be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appsync-datasource-description"></a>
The description of the data source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBConfig`  <a name="cfn-appsync-datasource-dynamodbconfig"></a>
AwsRegion and TableName for an Amazon DynamoDB table in your account\.  
*Required*: No  
*Type*: [DynamoDBConfig](aws-properties-appsync-datasource-dynamodbconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticsearchConfig`  <a name="cfn-appsync-datasource-elasticsearchconfig"></a>
AwsRegion and Endpoints for an Amazon Elasticsearch Service domain in your account\.  
*Required*: No  
*Type*: [ElasticsearchConfig](aws-properties-appsync-datasource-elasticsearchconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpConfig`  <a name="cfn-appsync-datasource-httpconfig"></a>
Endpoints for an HTTP data source\.  
*Required*: No  
*Type*: [HttpConfig](aws-properties-appsync-datasource-httpconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaConfig`  <a name="cfn-appsync-datasource-lambdaconfig"></a>
An ARN of a Lambda function in valid ARN format\. This can be the ARN of a Lambda function that exists in the current account or in another account\.  
*Required*: No  
*Type*: [LambdaConfig](aws-properties-appsync-datasource-lambdaconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appsync-datasource-name"></a>
Friendly name for you to identify your AppSync data source after creation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RelationalDatabaseConfig`  <a name="cfn-appsync-datasource-relationaldatabaseconfig"></a>
Relational Database configuration of the relational database data source\.  
*Required*: No  
*Type*: [RelationalDatabaseConfig](aws-properties-appsync-datasource-relationaldatabaseconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-appsync-datasource-servicerolearn"></a>
The AWS IAM service role ARN for the data source\. The system assumes this role when accessing the data source\.  
Required if `Type` is specified as `AWS_LAMBDA`, `AMAZON_DYNAMODB`, or `AMAZON_ELASTICSEARCH`\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-appsync-datasource-type"></a>
The type of the data source\.  
+  **AMAZON\_DYNAMODB**: The data source is an Amazon DynamoDB table\.
+  **AMAZON\_ELASTICSEARCH**: The data source is an Amazon Elasticsearch Service domain\.
+  **AWS\_LAMBDA**: The data source is an AWS Lambda function\.
+  **NONE**: There is no data source\. This type is used when you wish to invoke a GraphQL operation without connecting to a data source, such as performing data transformation with resolvers or triggering a subscription to be invoked from a mutation\.
+  **HTTP**: The data source is an HTTP endpoint\.
+  **RELATIONAL\_DATABASE**: The data source is a relational database\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appsync-datasource-return-values"></a>

### Ref<a name="aws-resource-appsync-datasource-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::DataSource` resource to the intrinsic `Ref` function, the function returns the ARN of the Data Source, such as ` arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/datasources/datasourcename`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.

### Fn::GetAtt<a name="aws-resource-appsync-datasource-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-datasource-return-values-fn--getatt-fn--getatt"></a>

`DataSourceArn`  <a name="DataSourceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/datasources/datasourcename`\. 

`Name`  <a name="Name-fn::getatt"></a>
Friendly name for you to identify your AppSync data source after creation\.

## Examples<a name="aws-resource-appsync-datasource--examples"></a>



### Data Source Creation Example<a name="aws-resource-appsync-datasource--examples--Data_Source_Creation_Example"></a>

The following example creates a data source and associates it with an existing GraphQL API by passing the GraphQL API ID as a parameter\. 

#### YAML<a name="aws-resource-appsync-datasource--examples--Data_Source_Creation_Example--yaml"></a>

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
    Type: AWS::AppSync::DataSource
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

#### JSON<a name="aws-resource-appsync-datasource--examples--Data_Source_Creation_Example--json"></a>

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

## See also<a name="aws-resource-appsync-datasource--seealso"></a>
+  [CreateDataSource](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateDataSource.html) operation in the *AWS AppSync API Reference*\.

