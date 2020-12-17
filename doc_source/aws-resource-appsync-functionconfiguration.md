# AWS::AppSync::FunctionConfiguration<a name="aws-resource-appsync-functionconfiguration"></a>

The `AWS::AppSync::FunctionConfiguration` resource defines the functions in GraphQL APIs to perform certain operations\. You can use pipeline resolvers to attach functions\. For more information, see [Pipeline Resolvers](https://docs.aws.amazon.com/appsync/latest/devguide/pipeline-resolvers.html) in the *AWS AppSync Developer Guide*\. 

**Note**  
When you submit an update, AWS CloudFormation updates resources based on differences between what you submit and the stack's current template\. To cause this resource to be updated you must change a property value for this resource in the CloudFormation template\. Changing the S3 file content without changing a property value will not result in an update operation\.  
See [Update Behaviors of Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html) in the *AWS CloudFormation User Guide*\.

## Syntax<a name="aws-resource-appsync-functionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-functionconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::FunctionConfiguration",
  "Properties" : {
      "[ApiId](#cfn-appsync-functionconfiguration-apiid)" : String,
      "[DataSourceName](#cfn-appsync-functionconfiguration-datasourcename)" : String,
      "[Description](#cfn-appsync-functionconfiguration-description)" : String,
      "[FunctionVersion](#cfn-appsync-functionconfiguration-functionversion)" : String,
      "[Name](#cfn-appsync-functionconfiguration-name)" : String,
      "[RequestMappingTemplate](#cfn-appsync-functionconfiguration-requestmappingtemplate)" : String,
      "[RequestMappingTemplateS3Location](#cfn-appsync-functionconfiguration-requestmappingtemplates3location)" : String,
      "[ResponseMappingTemplate](#cfn-appsync-functionconfiguration-responsemappingtemplate)" : String,
      "[ResponseMappingTemplateS3Location](#cfn-appsync-functionconfiguration-responsemappingtemplates3location)" : String,
      "[SyncConfig](#cfn-appsync-functionconfiguration-syncconfig)" : SyncConfig
    }
}
```

### YAML<a name="aws-resource-appsync-functionconfiguration-syntax.yaml"></a>

```
Type: AWS::AppSync::FunctionConfiguration
Properties: 
  [ApiId](#cfn-appsync-functionconfiguration-apiid): String
  [DataSourceName](#cfn-appsync-functionconfiguration-datasourcename): String
  [Description](#cfn-appsync-functionconfiguration-description): String
  [FunctionVersion](#cfn-appsync-functionconfiguration-functionversion): String
  [Name](#cfn-appsync-functionconfiguration-name): String
  [RequestMappingTemplate](#cfn-appsync-functionconfiguration-requestmappingtemplate): String
  [RequestMappingTemplateS3Location](#cfn-appsync-functionconfiguration-requestmappingtemplates3location): String
  [ResponseMappingTemplate](#cfn-appsync-functionconfiguration-responsemappingtemplate): String
  [ResponseMappingTemplateS3Location](#cfn-appsync-functionconfiguration-responsemappingtemplates3location): String
  [SyncConfig](#cfn-appsync-functionconfiguration-syncconfig): 
    SyncConfig
```

## Properties<a name="aws-resource-appsync-functionconfiguration-properties"></a>

`ApiId`  <a name="cfn-appsync-functionconfiguration-apiid"></a>
The AWS AppSync GraphQL API that you want to attach using this function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSourceName`  <a name="cfn-appsync-functionconfiguration-datasourcename"></a>
The name of data source this function will attach\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appsync-functionconfiguration-description"></a>
The `Function` description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionVersion`  <a name="cfn-appsync-functionconfiguration-functionversion"></a>
The version of the request mapping template\. Currently only the 2018\-05\-29 version of the template is supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appsync-functionconfiguration-name"></a>
The name of the function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestMappingTemplate`  <a name="cfn-appsync-functionconfiguration-requestmappingtemplate"></a>
The `Function` request mapping template\. Functions support only the 2018\-05\-29 version of the request mapping template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestMappingTemplateS3Location`  <a name="cfn-appsync-functionconfiguration-requestmappingtemplates3location"></a>
The location of a request mapping template in an Amazon S3 bucket\. Use this if you want to provision with a template file in Amazon S3 rather than embedding it in your CloudFormation template\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseMappingTemplate`  <a name="cfn-appsync-functionconfiguration-responsemappingtemplate"></a>
The `Function` response mapping template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseMappingTemplateS3Location`  <a name="cfn-appsync-functionconfiguration-responsemappingtemplates3location"></a>
The location of a response mapping template in an Amazon S3 bucket\. Use this if you want to provision with a template file in Amazon S3 rather than embedding it in your CloudFormation template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SyncConfig`  <a name="cfn-appsync-functionconfiguration-syncconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [SyncConfig](aws-properties-appsync-functionconfiguration-syncconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appsync-functionconfiguration-return-values"></a>

### Ref<a name="aws-resource-appsync-functionconfiguration-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::FunctionConfiguration` resource to the intrinsic `Ref` function, the function returns the ARN of the FunctionConfiguration, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/functions/functionid`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.

### Fn::GetAtt<a name="aws-resource-appsync-functionconfiguration-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-functionconfiguration-return-values-fn--getatt-fn--getatt"></a>

`DataSourceName`  <a name="DataSourceName-fn::getatt"></a>
The name of data source this function will attach\.

`FunctionArn`  <a name="FunctionArn-fn::getatt"></a>
ARN of the function, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/functions/functionId`\.

`FunctionId`  <a name="FunctionId-fn::getatt"></a>
The unique ID of this function\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the function\.

## Examples<a name="aws-resource-appsync-functionconfiguration--examples"></a>



### Function Creation Example<a name="aws-resource-appsync-functionconfiguration--examples--Function_Creation_Example"></a>

The following example creates a function and associates it with an existing GraphQL API and a data source by passing the GraphQL API ID and data source name as a parameter\.

#### YAML<a name="aws-resource-appsync-functionconfiguration--examples--Function_Creation_Example--yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  dataSourceName:
    Type: String
  name:
    Type: String
  description:
    Type: String
  functionVersion:
    Type: String
  requestMappingTemplateS3LocationInput:
    Type: String
  responseMappingTemplateS3LocationInput:
    Type: String
Resources:
  FunctionConfiguration:
    Type: AWS::AppSync::FunctionConfiguration
    Properties:
      ApiId:
	Ref: graphQlApiId
      Name:
        Ref: name
      Description:
        Ref: description
      DataSourceName:
        Ref: dataSourceName
      FunctionVersion:
        Ref: functionVersion
      RequestMappingTemplateS3Location:
        Ref: requestMappingTemplateS3LocationInput
      ResponseMappingTemplateS3Location:
        Ref: responseMappingTemplateS3LocationInput
```

#### JSON<a name="aws-resource-appsync-functionconfiguration--examples--Function_Creation_Example--json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "name": {
      "Type": "String"
    },
    "description": {
      "Type": "String"
    },
    "dataSourceName": {
      "Type": "String"
    },
    "functionVersion": {
      "Type": "String"
    },
    "requestMappingTemplateS3LocationInput": {
      "Type": "String"
    },
    "responseMappingTemplateS3LocationInput": {
      "Type": "String"
    }
  },
  "Resources": {
    "FunctionConfiguration": {
      "Type": "AWS::AppSync::FunctionConfiguration",
      "Properties": {
        "ApiId": {
          "Ref": "graphQlApiId"
        },
        "Name": {
          "Ref": "name"
        },
        "Description": {
          "Ref": "description"
        },
        "FunctionVersion": {
          "Ref": "functionVersion"
        },
        "DataSourceName": {
          "Ref": "dataSourceName"
        },
        "RequestMappingTemplateS3Location": {
          "Ref": "requestMappingTemplateS3LocationInput"
        },
        "ResponseMappingTemplateS3Location": {
          "Ref": "responseMappingTemplateS3LocationInput"
        }
      }
    }
  }
}
```

## See also<a name="aws-resource-appsync-functionconfiguration--seealso"></a>
+  [CreateFunction](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateFunction.html) operation in the *AWS AppSync API Reference*\.

