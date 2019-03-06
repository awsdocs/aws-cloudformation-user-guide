# AWS::AppSync::FunctionConfiguration<a name="aws-resource-appsync-functionconfiguration"></a>

The `AWS::AppSync::FunctionConfiguration` resource defines the functions in GraphQL Apis to perform certain operations\. Functions can be attached by PipelineResolver\. More information on functions can be found in the [https://docs.aws.amazon.com/appsync/latest/devguide/function.html](https://docs.aws.amazon.com/appsync/latest/devguide/function.html)\.  

**Topics**
+ [Syntax](#aws-resource-appsync-functionconfiguration-syntax)
+ [Properties](#aws-resource-appsync-functionconfiguration-properties)
+ [Return Values](#aws-resource-appsync-functionconfiguration-returnvalues)
+ [Examples](#aws-resource-appsync-functionconfiguration-examples)
+ [See Also](#aws-resource-appsync-functionconfiguration-seealso)

## Syntax<a name="aws-resource-appsync-functionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-functionconfiguration-syntax.json"></a>

```
{
    "Type" : "AWS::AppSync::FunctionConfiguration",
    "Properties" : {
      "[ApiId](#cfn-appsync-functionconfiguration-apiid)" : String,
      "[Name](#cfn-appsync-functionconfiguration-name)" : String,
      "[Description](#cfn-appsync-functionconfiguration-description)" : String,
      "[DataSourceName](#cfn-appsync-functionconfiguration-datasourcename)" : String,
      "[FunctionVersion](#cfn-appsync-functionconfiguration-functionversion)" : String,
      "[RequestMappingTemplate](#cfn-appsync-functionconfiguration-requestmappingtemplate)" : String,
      "[RequestMappingTemplateS3Location](#cfn-appsync-functionconfiguration-requestmappingtemplates3location)" : String,
      "[ResponseMappingTemplate](#cfn-appsync-functionconfiguration-responsemappingtemplate)" : String,
      "[ResponseMappingTemplateS3Location](#cfn-appsync-functionconfiguration-responsemappingtemplates3location)" : String
    }
 }
```

### YAML<a name="aws-resource-appsync-functionconfiguration-syntax.yaml"></a>

```
Type: "AWS::AppSync::FunctionConfiguration"
Properties:
  [ApiId](#cfn-appsync-functionconfiguration-apiid): String
  [Name](#cfn-appsync-functionconfiguration-name): String
  [Description](#cfn-appsync-functionconfiguration-description): String
  [DataSourceName](#cfn-appsync-functionconfiguration-datasourcename): String
  [FunctionVersion](#cfn-appsync-functionconfiguration-functionversion): String
  [RequestMappingTemplate](#cfn-appsync-functionconfiguration-requestmappingtemplate): String
  [RequestMappingTemplateS3Location](#cfn-appsync-functionconfiguration-requestmappingtemplates3location): String
  [ResponseMappingTemplate](#cfn-appsync-functionconfiguration-responsemappingtemplate): String
  [ResponseMappingTemplateS3Location](#cfn-appsync-functionconfiguration-responsemappingtemplates3location): String
```

## Properties<a name="aws-resource-appsync-functionconfiguration-properties"></a>

`ApiId`  <a name="cfn-appsync-functionconfiguration-apiid"></a>
The AWS AppSync GraphQL API which you will attach with this function\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-appsync-functionconfiguration-name"></a>
The Name of the function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-appsync-functionconfiguration-description"></a>
The Description of the function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DataSourceName`  <a name="cfn-appsync-functionconfiguration-datasourcename"></a>
The AWS AppSync data source that this function will run against in order to return data to the caller\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FunctionVersion`  <a name="cfn-appsync-functionconfiguration-functionversion"></a>
The version of the function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RequestMappingTemplate`  <a name="cfn-appsync-functionconfiguration-requestmappingtemplate"></a>
The function’s request mapping template, written in text within the CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RequestMappingTemplateS3Location`  <a name="cfn-appsync-functionconfiguration-requestmappingtemplates3location"></a>
A location of a request mapping template on an S3 bucket if you wish to provision with the template file living in S3 rather than embedded in your CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseMappingTemplate`  <a name="cfn-appsync-functionconfiguration-responsemappingtemplate"></a>
The function’s response mapping template, written in text within the CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseMappingTemplateS3Location`  <a name="cfn-appsync-functionconfiguration-responsemappingtemplates3location"></a>
A location of a response mapping template on an S3 bucket if you wish to provision with the template file living in S3 rather than embedded in your CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-appsync-functionconfiguration-returnvalues"></a>

### Ref<a name="aws-resource-appsync-functionconfiguration-ref"></a>

When you pass the logical ID of an `AWS::AppSync::FunctionConfiguration` resource to the intrinsic `Ref` function, the function returns the ARN of the FunctionConfiguration, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/functions/functionid`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-appsync-functionconfiguration-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`FunctionName`  
The name of this function\. 

`FunctionArn`  
ARN of the Function, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/functions/functionId`\. 

`FunctionId`  
The unique Id of this function\. 

`DataSourceName`  
The name of data source this function will attach\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-appsync-functionconfiguration-examples"></a>

### Function creation example<a name="aws-resource-appsync-functionconfiguration-example1"></a>

The following example creates a function and associates it with an existing GraphQL API and a data source by passing the GraphQL API Id and data source name as a paramater\.

#### JSON<a name="aws-resource-appsync-functionconfiguration-example1.json"></a>

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

#### YAML<a name="aws-resource-appsync-functionconfiguration-example1.yaml"></a>

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

## See Also<a name="aws-resource-appsync-functionconfiguration-seealso"></a>
+ [ CreateFunction](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateFunction.html) operation in the *AWS AppSync API Reference*