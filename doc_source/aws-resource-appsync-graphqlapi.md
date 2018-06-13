# AWS::AppSync::GraphQLApi<a name="aws-resource-appsync-graphqlapi"></a>

The `AWS::AppSync::GraphQLApi` resource will create a new AWS AppSync GraphQL API\. This is the top level construct for your application\. For more information see [http://docs.aws.amazon.com/appsync/latest/devguide/quickstart.html](http://docs.aws.amazon.com/appsync/latest/devguide/quickstart.html)\. 

**Topics**
+ [Syntax](#aws-resource-appsync-graphqlapi-syntax)
+ [Properties](#aws-resource-appsync-graphqlapi-properties)
+ [Return Values](#aws-resource-appsync-graphqlapi-returnvalues)
+ [Examples](#aws-resource-appsync-graphqlapi-examples)
+ [See Also](#aws-resource-appsync-graphqlapi-seealso)

## Syntax<a name="aws-resource-appsync-graphqlapi-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-graphqlapi-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::GraphQLApi",
  "Properties" : {
    "[UserPoolConfig](#cfn-appsync-graphqlapi-userpoolconfig)" : [*UserPoolConfig*](aws-properties-appsync-graphqlapi-userpoolconfig.md),
    "[OpenIDConnectConfig](#cfn-appsync-graphqlapi-openidconnectconfig)" : [*OpenIDConnectConfig*](aws-properties-appsync-graphqlapi-openidconnectconfig.md),
    "[Name](#cfn-appsync-graphqlapi-name)" : String,
    "[AuthenticationType](#cfn-appsync-graphqlapi-authenticationtype)" : String,
    "[LogConfig](#cfn-appsync-graphqlapi-logconfig)" : [*LogConfig*](aws-properties-appsync-graphqlapi-logconfig.md)
  }
}
```

### YAML<a name="aws-resource-appsync-graphqlapi-syntax.yaml"></a>

```
Type: "AWS::AppSync::GraphQLApi"
Properties:
  [UserPoolConfig](#cfn-appsync-graphqlapi-userpoolconfig): [*UserPoolConfig*](aws-properties-appsync-graphqlapi-userpoolconfig.md)
  [OpenIDConnectConfig](#cfn-appsync-graphqlapi-openidconnectconfig) : [*OpenIDConnectConfig*](aws-properties-appsync-graphqlapi-openidconnectconfig.md)
  [Name](#cfn-appsync-graphqlapi-name): String
  [AuthenticationType](#cfn-appsync-graphqlapi-authenticationtype): String
  [LogConfig](#cfn-appsync-graphqlapi-logconfig): [*LogConfig*](aws-properties-appsync-graphqlapi-logconfig.md)
```

## Properties<a name="aws-resource-appsync-graphqlapi-properties"></a>

`UserPoolConfig`  <a name="cfn-appsync-graphqlapi-userpoolconfig"></a>
Optional authorization configuration for using Amazon Cognito User Pools with your GraphQL endpoint\.  
 *Required*: No  
 *Type*: [AWS AppSync GraphQLApi UserPoolConfig](aws-properties-appsync-graphqlapi-userpoolconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OpenIDConnectConfig`  <a name="cfn-appsync-graphqlapi-openidconnectconfig"></a>
Optional authorization configuration for using an OpenId Connect compliant service with your GraphQL endpoint\.  
 *Required*: No  
 *Type*: [AWS AppSync GraphQLApi OpenId Connect Config](aws-properties-appsync-graphqlapi-openidconnectconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-appsync-graphqlapi-name"></a>
Friendly name for your GraphQL API in AWS AppSync\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthenticationType`  <a name="cfn-appsync-graphqlapi-authenticationtype"></a>
Security configuration for your GraphQL API\. For allowed values \(such as API\_KEY, AWS\_IAM, or AMAZON\_COGNITO\_USER\_POOLS, OPENID\_CONNECT\), see [Security](http://docs.aws.amazon.com/appsync/latest/devguide/security.html) in the *AWS AppSync Developer Guide*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LogConfig`  <a name="cfn-appsync-graphqlapi-logconfig"></a>
Logging configuration when writing GraphQL operations and tracing to Amazon Cloudwatch\.  
 *Required*: No  
 *Type*: [AWS AppSync GraphQLApi LogConfig](aws-properties-appsync-graphqlapi-logconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-appsync-graphqlapi-returnvalues"></a>

### Ref<a name="aws-resource-appsync-graphqlapi-ref"></a>

When you pass the logical ID of an `AWS::AppSync::GraphQLApi` resource to the intrinsic `Ref` function, the function returns the ARN of the GraphQL API, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-appsync-graphqlapi-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`GraphQLUrl`  
The Endpoint URL of your GraphQL API\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid`\. 

`ApiId`  
Unique AWS AppSync GraphQL API Identifier\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-appsync-graphqlapi-examples"></a>

### GraphQL API creation example<a name="aws-resource-appsync-graphqlapi-example1"></a>

The following example creates a GraphQL API

#### JSON<a name="aws-resource-appsync-graphqlapi-example1.json"></a>

```
{
  "Parameters": {
    "graphQlApiName": {
      "Type": "String"
    },
    "userPoolId": {
      "Type": "String"
    },
    "userPoolAwsRegion": {
      "Type": "String"
    },
    "defaultAction": {
      "Type": "String"
    }
  },
  "Resources": {
    "GraphQLApi": {
      "Type": "AWS::AppSync::GraphQLApi",
      "Properties": {
        "Name": {
          "Ref": "graphQlApiName"
        },
        "AuthenticationType": "AMAZON_COGNITO_USER_POOLS",
        UserPoolConfig": {
          "UserPoolId": {
            "Ref": "userPoolId"
          },
          "AwsRegion": {
            "Ref": "userPoolAwsRegion"
          },
          "DefaultAction": {
            "Ref": "defaultAction"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appsync-graphqlapi-example1.yaml"></a>

```
Parameters:
  graphQlApiName:
    Type: String
  userPoolId:
    Type: String
  userPoolAwsRegion:
    Type: String
  defaultAction:
    Type: String
Resources:
  GraphQLApi:
    Type: "AWS::AppSync::GraphQLApi"
    Properties:
      Name:
	Ref: graphQlApiName
      AuthenticationType: "AMAZON_COGNITO_USER_POOLS"
      "UserPoolConfig":
        UserPoolId:
          Ref: userPoolId
        AwsRegion:
          Ref: userPoolAwsRegion
        DefaultAction:
          Ref: defaultAction
```

## See Also<a name="aws-resource-appsync-graphqlapi-seealso"></a>
+ [ CreateGraphqlApi](http://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateGraphqlApi.html) operation in the *AWS AppSync API Reference*