# AWS::AppSync::GraphQLSchema<a name="aws-resource-appsync-graphqlschema"></a>

The `AWS::AppSync::GraphQLSchema` resource is used for your AWS AppSync GraphQL schema which controls the data model for your API\. Schema files are text written in Schema Definition Language \(SDL\) format\. You can find information on schema authoring at [http://docs.aws.amazon.com/appsync/latest/devguide/designing-a-graphql-api.html](http://docs.aws.amazon.com/appsync/latest/devguide/designing-a-graphql-api.html)\. 

**Topics**
+ [Syntax](#aws-resource-appsync-graphqlschema-syntax)
+ [Properties](#aws-resource-appsync-graphqlschema-properties)
+ [Return Values](#aws-resource-appsync-graphqlschema-returnvalues)
+ [Examples](#aws-resource-appsync-graphqlschema-examples)
+ [See Also](#aws-resource-appsync-graphqlschema-seealso)

## Syntax<a name="aws-resource-appsync-graphqlschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-graphqlschema-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::GraphQLSchema",
  "Properties" : {
    "[Definition](#cfn-appsync-graphqlschema-definition)" : String,
    "[DefinitionS3Location](#cfn-appsync-graphqlschema-definitions3location)" : String,
    "[ApiId](#cfn-appsync-graphqlschema-apiid)" : String
  }
}
```

### YAML<a name="aws-resource-appsync-graphqlschema-syntax.yaml"></a>

```
Type: "AWS::AppSync::GraphQLSchema"
Properties:
  [Definition](#cfn-appsync-graphqlschema-definition): String
  [DefinitionS3Location](#cfn-appsync-graphqlschema-definitions3location): String
  [ApiId](#cfn-appsync-graphqlschema-apiid): String
```

## Properties<a name="aws-resource-appsync-graphqlschema-properties"></a>

`Definition`  <a name="cfn-appsync-graphqlschema-definition"></a>
The text representation of a GraphQL schema in SDL format\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DefinitionS3Location`  <a name="cfn-appsync-graphqlschema-definitions3location"></a>
A location of a GraphQL schema file on an S3 bucket if you wish to provision with the schema living in S3 rather than embedded in your CloudFormation template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApiId`  <a name="cfn-appsync-graphqlschema-apiid"></a>
The AWS AppSync GraphQL API identifier to which you will apply this schema\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-appsync-graphqlschema-returnvalues"></a>

### Ref<a name="aws-resource-appsync-graphqlschema-ref"></a>

When you pass the logical ID of an `AWS::AppSync::GraphQLSchema` resource to the intrinsic `Ref` function, the function returns the GraphQL API id with the literal String GraphQLSchema attached to it\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-appsync-graphqlschema-examples"></a>

### GraphQL Schema creation example<a name="aws-resource-appsync-graphqlschema-example1"></a>

The following example creates a GraphQL Schema and associates it with an existing GraphQL API by passing the GraphQL API Id as a paramater\.

#### JSON<a name="aws-resource-appsync-graphqlschema-example1.json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "graphQlSchemaS3DescriptionLocation": {
      "Type": "String"
    }
  },
  "Resources": {
    "Schema": {
      "Type": "AWS::AppSync::GraphQLSchema",
      "Properties": {
        "ApiId": {
          "Ref": "graphQlApiId"
        },
        "DefinitionS3Location": {
          "Ref": "graphQlSchemaS3DescriptionLocation"
        }
      }       
    }
  }
}
```

#### YAML<a name="aws-resource-appsync-graphqlschema-example1.yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  graphQlSchemaS3DescriptionLocation:
    Type: String
Resources:
  Schema:
    Type: "AWS::AppSync::GraphQLSchema"
    Properties:
      ApiId:
	Ref: graphQlApiId
      DefinitionS3Location:
        Ref: graphQlSchemaS3DescriptionLocation
```

## See Also<a name="aws-resource-appsync-graphqlschema-seealso"></a>
+ [ StartSchemaCreation](http://docs.aws.amazon.com/appsync/latest/APIReference/API_StartSchemaCreation.html) operation in the *AWS AppSync API Reference*