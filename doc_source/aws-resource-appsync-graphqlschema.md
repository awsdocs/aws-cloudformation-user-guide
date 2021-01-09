# AWS::AppSync::GraphQLSchema<a name="aws-resource-appsync-graphqlschema"></a>

The `AWS::AppSync::GraphQLSchema` resource is used for your AWS AppSync GraphQL schema that controls the data model for your API\. Schema files are text written in Schema Definition Language \(SDL\) format\. For more information about schema authoring, see [Designing a GraphQL API](https://docs.aws.amazon.com/appsync/latest/devguide/designing-a-graphql-api.html) in the *AWS AppSync Developer Guide*\.

**Note**  
When you submit an update, AWS CloudFormation updates resources based on differences between what you submit and the stack's current template\. To cause this resource to be updated you must change a property value for this resource in the CloudFormation template\. Changing the S3 file content without changing a property value will not result in an update operation\.  
See [Update Behaviors of Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html) in the *AWS CloudFormation User Guide*\.

## Syntax<a name="aws-resource-appsync-graphqlschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-graphqlschema-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::GraphQLSchema",
  "Properties" : {
      "[ApiId](#cfn-appsync-graphqlschema-apiid)" : String,
      "[Definition](#cfn-appsync-graphqlschema-definition)" : String,
      "[DefinitionS3Location](#cfn-appsync-graphqlschema-definitions3location)" : String
    }
}
```

### YAML<a name="aws-resource-appsync-graphqlschema-syntax.yaml"></a>

```
Type: AWS::AppSync::GraphQLSchema
Properties: 
  [ApiId](#cfn-appsync-graphqlschema-apiid): String
  [Definition](#cfn-appsync-graphqlschema-definition): String
  [DefinitionS3Location](#cfn-appsync-graphqlschema-definitions3location): String
```

## Properties<a name="aws-resource-appsync-graphqlschema-properties"></a>

`ApiId`  <a name="cfn-appsync-graphqlschema-apiid"></a>
The AWS AppSync GraphQL API identifier to which you want to apply this schema\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Definition`  <a name="cfn-appsync-graphqlschema-definition"></a>
The text representation of a GraphQL schema in SDL format\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefinitionS3Location`  <a name="cfn-appsync-graphqlschema-definitions3location"></a>
The location of a GraphQL schema file in an Amazon S3 bucket\. Use this if you want to provision with the schema living in Amazon S3 rather than embedding it in your CloudFormation template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appsync-graphqlschema-return-values"></a>

### Ref<a name="aws-resource-appsync-graphqlschema-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::GraphQLSchema` resource to the intrinsic `Ref` function, the function returns the GraphQL API id with the literal String GraphQLSchema attached to it\. 

## Examples<a name="aws-resource-appsync-graphqlschema--examples"></a>



### GraphQL Schema Creation Example<a name="aws-resource-appsync-graphqlschema--examples--GraphQL_Schema_Creation_Example"></a>

The following example creates a GraphQL Schema and associates it with an existing GraphQL API by passing the GraphQL API ID as a parameter\.

#### YAML<a name="aws-resource-appsync-graphqlschema--examples--GraphQL_Schema_Creation_Example--yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  graphQlSchemaS3DescriptionLocation:
    Type: String
Resources:
  Schema:
    Type: AWS::AppSync::GraphQLSchema
    Properties:
      ApiId:
	Ref: graphQlApiId
      DefinitionS3Location:
        Ref: graphQlSchemaS3DescriptionLocation
```

#### JSON<a name="aws-resource-appsync-graphqlschema--examples--GraphQL_Schema_Creation_Example--json"></a>

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

## See also<a name="aws-resource-appsync-graphqlschema--seealso"></a>
+  [StartSchemaCreation](https://docs.aws.amazon.com/appsync/latest/APIReference/API_StartSchemaCreation.html) operation in the *AWS AppSync API Reference*\.

