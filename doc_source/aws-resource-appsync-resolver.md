# AWS::AppSync::Resolver<a name="aws-resource-appsync-resolver"></a>

The `AWS::AppSync::Resolver` resource defines the logical GraphQL resolver that you will attach to fields in a schema\. Request and Response templates for resolvers are written in Apache Velocity Template Language \(VTL\) format\. More information on resolvers can be found in the [http://docs.aws.amazon.com/appsync/latest/devguide/resolver-mapping-template-reference.html](http://docs.aws.amazon.com/appsync/latest/devguide/resolver-mapping-template-reference.html)\. 

**Topics**
+ [Syntax](#aws-resource-appsync-resolver-syntax)
+ [Properties](#aws-resource-appsync-resolver-properties)
+ [Return Values](#aws-resource-appsync-resolver-returnvalues)
+ [Examples](#aws-resource-appsync-resolver-examples)
+ [See Also](#aws-resource-appsync-resolver-seealso)

## Syntax<a name="aws-resource-appsync-resolver-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-resolver-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::Resolver",
  "Properties" : {
    "[ResponseMappingTemplateS3Location](#cfn-appsync-resolver-responsemappingtemplates3location)" : String,
    "[TypeName](#cfn-appsync-resolver-typename)" : String,
    "[DataSourceName](#cfn-appsync-resolver-datasourcename)" : String,
    "[RequestMappingTemplate](#cfn-appsync-resolver-requestmappingtemplate)" : String,
    "[ResponseMappingTemplate](#cfn-appsync-resolver-responsemappingtemplate)" : String,
    "[RequestMappingTemplateS3Location](#cfn-appsync-resolver-requestmappingtemplates3location)" : String,
    "[ApiId](#cfn-appsync-resolver-apiid)" : String,
    "[FieldName](#cfn-appsync-resolver-fieldname)" : String
  }
}
```

### YAML<a name="aws-resource-appsync-resolver-syntax.yaml"></a>

```
Type: "AWS::AppSync::Resolver"
Properties:
  [ResponseMappingTemplateS3Location](#cfn-appsync-resolver-responsemappingtemplates3location): String
  [TypeName](#cfn-appsync-resolver-typename): String
  [DataSourceName](#cfn-appsync-resolver-datasourcename): String
  [RequestMappingTemplate](#cfn-appsync-resolver-requestmappingtemplate): String
  [ResponseMappingTemplate](#cfn-appsync-resolver-responsemappingtemplate): String
  [RequestMappingTemplateS3Location](#cfn-appsync-resolver-requestmappingtemplates3location): String
  [ApiId](#cfn-appsync-resolver-apiid): String
  [FieldName](#cfn-appsync-resolver-fieldname): String
```

## Properties<a name="aws-resource-appsync-resolver-properties"></a>

`ResponseMappingTemplateS3Location`  <a name="cfn-appsync-resolver-responsemappingtemplates3location"></a>
A location of a response mapping template on an S3 bucket if you wish to provision with the template file living in S3 rather than embedded in your CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TypeName`  <a name="cfn-appsync-resolver-typename"></a>
The GraphQL type that will invoke this resolver\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DataSourceName`  <a name="cfn-appsync-resolver-datasourcename"></a>
The AWS AppSync data source that this resolver will run against in order to return data to the caller\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RequestMappingTemplate`  <a name="cfn-appsync-resolver-requestmappingtemplate"></a>
The resolver’s request mapping template, written in text within the CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseMappingTemplate`  <a name="cfn-appsync-resolver-responsemappingtemplate"></a>
 The resolver’s response mapping template, written in text within the CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RequestMappingTemplateS3Location`  <a name="cfn-appsync-resolver-requestmappingtemplates3location"></a>
A location of a request mapping template on an S3 bucket if you wish to provision with the template file living in S3 rather than embedded in your CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApiId`  <a name="cfn-appsync-resolver-apiid"></a>
The AWS AppSync GraphQL API which you will attach this resolver\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FieldName`  <a name="cfn-appsync-resolver-fieldname"></a>
The GraphQL field on a type that will invoke the resolver\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-appsync-resolver-returnvalues"></a>

### Ref<a name="aws-resource-appsync-resolver-ref"></a>

When you pass the logical ID of an `AWS::AppSync::Resolver` resource to the intrinsic `Ref` function, the function returns the ARN of the Resolver, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/types/typename/resolvers/resolvername`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-appsync-resolver-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`TypeName`  
The GraphQL type that will invoke this resolver\. 

`ResolverArn`  
ARN of the Resolver, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/types/typename/resolvers/resolvername`\. 

`FieldName`  
The GraphQL field on a type that will invoke the resolver\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-appsync-resolver-examples"></a>

### Resolver creation example<a name="aws-resource-appsync-resolver-example1"></a>

The following example creates a resolver and associates it with an existing GraphQL API and a data source by passing the GraphQL API Id and data source name as a paramater\.

#### JSON<a name="aws-resource-appsync-resolver-example1.json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "dataSourceName": {
      "Type": "String"
    },
    "fieldName": {
      "Type": "String"
    },
    "typeName": {
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
    "Resolver": {
      "Type": "AWS::AppSync::Resolver",
      "Properties": {
        "ApiId": {
          "Ref": "graphQlApiId"
        },
        "TypeName": {
          "Ref": "typeName"
        },
        "FieldName": {
          "Ref": "fieldName"
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

#### YAML<a name="aws-resource-appsync-resolver-example1.yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  dataSourceName:
    Type: String
  fieldName:
    Type: String
  typeName:
    Type: String
  requestMappingTemplateS3LocationInput:
    Type: String
  responseMappingTemplateS3LocationInput:
    Type: String
Resources:
  Resolver:
    Type: "AWS::AppSync::Resolver"
    Properties:
      ApiId:
	Ref: graphQlApiId
      TypeName:
        Ref: typeName
      FieldName:
        Ref: fieldName
      DataSourceName:
        Ref: dataSourceName
      RequestMappingTemplateS3Location:
        Ref: requestMappingTemplateS3LocationInput
      ResponseMappingTemplateS3Location:
        Ref: responseMappingTemplateS3LocationInput
```

## See Also<a name="aws-resource-appsync-resolver-seealso"></a>
+ [ CreateResolver](http://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateResolver.html) operation in the *AWS AppSync API Reference*