# AWS::AppSync::GraphQLApi<a name="aws-resource-appsync-graphqlapi"></a>

The `AWS::AppSync::GraphQLApi` resource creates a new AWS AppSync GraphQL API\. This is the top\-level construct for your application\. For more information, see [Quick Start](https://docs.aws.amazon.com/appsync/latest/devguide/quickstart.html) in the *AWS AppSync Developer Guide*\.

## Syntax<a name="aws-resource-appsync-graphqlapi-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-graphqlapi-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::GraphQLApi",
  "Properties" : {
      "[AdditionalAuthenticationProviders](#cfn-appsync-graphqlapi-additionalauthenticationproviders)" : [ AdditionalAuthenticationProvider, ... ],
      "[ApiType](#cfn-appsync-graphqlapi-apitype)" : String,
      "[AuthenticationType](#cfn-appsync-graphqlapi-authenticationtype)" : String,
      "[LambdaAuthorizerConfig](#cfn-appsync-graphqlapi-lambdaauthorizerconfig)" : LambdaAuthorizerConfig,
      "[LogConfig](#cfn-appsync-graphqlapi-logconfig)" : LogConfig,
      "[MergedApiExecutionRoleArn](#cfn-appsync-graphqlapi-mergedapiexecutionrolearn)" : String,
      "[Name](#cfn-appsync-graphqlapi-name)" : String,
      "[OpenIDConnectConfig](#cfn-appsync-graphqlapi-openidconnectconfig)" : OpenIDConnectConfig,
      "[OwnerContact](#cfn-appsync-graphqlapi-ownercontact)" : String,
      "[Tags](#cfn-appsync-graphqlapi-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserPoolConfig](#cfn-appsync-graphqlapi-userpoolconfig)" : UserPoolConfig,
      "[Visibility](#cfn-appsync-graphqlapi-visibility)" : String,
      "[XrayEnabled](#cfn-appsync-graphqlapi-xrayenabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-appsync-graphqlapi-syntax.yaml"></a>

```
Type: AWS::AppSync::GraphQLApi
Properties: 
  [AdditionalAuthenticationProviders](#cfn-appsync-graphqlapi-additionalauthenticationproviders): 
    - AdditionalAuthenticationProvider
  [ApiType](#cfn-appsync-graphqlapi-apitype): String
  [AuthenticationType](#cfn-appsync-graphqlapi-authenticationtype): String
  [LambdaAuthorizerConfig](#cfn-appsync-graphqlapi-lambdaauthorizerconfig): 
    LambdaAuthorizerConfig
  [LogConfig](#cfn-appsync-graphqlapi-logconfig): 
    LogConfig
  [MergedApiExecutionRoleArn](#cfn-appsync-graphqlapi-mergedapiexecutionrolearn): String
  [Name](#cfn-appsync-graphqlapi-name): String
  [OpenIDConnectConfig](#cfn-appsync-graphqlapi-openidconnectconfig): 
    OpenIDConnectConfig
  [OwnerContact](#cfn-appsync-graphqlapi-ownercontact): String
  [Tags](#cfn-appsync-graphqlapi-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserPoolConfig](#cfn-appsync-graphqlapi-userpoolconfig): 
    UserPoolConfig
  [Visibility](#cfn-appsync-graphqlapi-visibility): String
  [XrayEnabled](#cfn-appsync-graphqlapi-xrayenabled): Boolean
```

## Properties<a name="aws-resource-appsync-graphqlapi-properties"></a>

`AdditionalAuthenticationProviders`  <a name="cfn-appsync-graphqlapi-additionalauthenticationproviders"></a>
A list of additional authentication providers for the `GraphqlApi` API\.  
*Required*: No  
*Type*: List of [AdditionalAuthenticationProvider](aws-properties-appsync-graphqlapi-additionalauthenticationprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApiType`  <a name="cfn-appsync-graphqlapi-apitype"></a>
The value that indicates whether the GraphQL API is a standard API \(`GRAPHQL`\) or merged API \(`MERGED`\)\.  
The following values are valid:   
`GRAPHQL | MERGED`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthenticationType`  <a name="cfn-appsync-graphqlapi-authenticationtype"></a>
Security configuration for your GraphQL API\. For allowed values \(such as `API_KEY`, `AWS_IAM`, `AMAZON_COGNITO_USER_POOLS`, `OPENID_CONNECT`, or `AWS_LAMBDA`\), see [Security](https://docs.aws.amazon.com/appsync/latest/devguide/security.html) in the *AWS AppSync Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaAuthorizerConfig`  <a name="cfn-appsync-graphqlapi-lambdaauthorizerconfig"></a>
A `LambdaAuthorizerConfig` holds configuration on how to authorize AWS AppSync API access when using the `AWS_LAMBDA` authorizer mode\. Be aware that an AWS AppSync API may have only one Lambda authorizer configured at a time\.  
*Required*: No  
*Type*: [LambdaAuthorizerConfig](aws-properties-appsync-graphqlapi-lambdaauthorizerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfig`  <a name="cfn-appsync-graphqlapi-logconfig"></a>
The Amazon CloudWatch Logs configuration\.  
*Required*: No  
*Type*: [LogConfig](aws-properties-appsync-graphqlapi-logconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MergedApiExecutionRoleArn`  <a name="cfn-appsync-graphqlapi-mergedapiexecutionrolearn"></a>
The AWS Identity and Access Management service role ARN for a merged API\. The AppSync service assumes this role on behalf of the Merged API to validate access to source APIs at runtime and to prompt the `AUTO_MERGE` to update the merged API endpoint with the source API changes automatically\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appsync-graphqlapi-name"></a>
The API name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenIDConnectConfig`  <a name="cfn-appsync-graphqlapi-openidconnectconfig"></a>
The OpenID Connect configuration\.  
*Required*: No  
*Type*: [OpenIDConnectConfig](aws-properties-appsync-graphqlapi-openidconnectconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerContact`  <a name="cfn-appsync-graphqlapi-ownercontact"></a>
The owner contact information for an API resource\.  
This field accepts any string input with a length of 0 \- 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appsync-graphqlapi-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this GraphQL API\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolConfig`  <a name="cfn-appsync-graphqlapi-userpoolconfig"></a>
Optional authorization configuration for using Amazon Cognito user pools with your GraphQL endpoint\.   
*Required*: No  
*Type*: [UserPoolConfig](aws-properties-appsync-graphqlapi-userpoolconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-appsync-graphqlapi-visibility"></a>
Sets the scope of the GraphQL API to public \(`GLOBAL`\) or private \(`PRIVATE`\)\. By default, the scope is set to `Global` if no value is provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`XrayEnabled`  <a name="cfn-appsync-graphqlapi-xrayenabled"></a>
A flag indicating whether to use AWS X\-Ray tracing for this `GraphqlApi`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appsync-graphqlapi-return-values"></a>

### Ref<a name="aws-resource-appsync-graphqlapi-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::GraphQLApi` resource to the intrinsic `Ref` function, the function returns the ARN of the GraphQL API, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.

### Fn::GetAtt<a name="aws-resource-appsync-graphqlapi-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-graphqlapi-return-values-fn--getatt-fn--getatt"></a>

`ApiId`  <a name="ApiId-fn::getatt"></a>
Unique AWS AppSync GraphQL API identifier\. 

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid`\. 

`GraphQLDns`  <a name="GraphQLDns-fn::getatt"></a>
The fully qualified domain name \(FQDN\) of the endpoint URL of your GraphQL API\.

`GraphQLUrl`  <a name="GraphQLUrl-fn::getatt"></a>
The Endpoint URL of your GraphQL API\. 

`RealtimeDns`  <a name="RealtimeDns-fn::getatt"></a>
The fully qualified domain name \(FQDN\) of the real\-time endpoint URL of your GraphQL API\.

`RealtimeUrl`  <a name="RealtimeUrl-fn::getatt"></a>
The GraphQL API real\-time endpoint URL\. For more information, see [Discovering the real\-time endpoint from the GraphQL endpoint](https://docs.aws.amazon.com/appsync/latest/devguide/real-time-websocket-client.html#handshake-details-to-establish-the-websocket-connection)\.

## Examples<a name="aws-resource-appsync-graphqlapi--examples"></a>



### GraphQL API Creation Example<a name="aws-resource-appsync-graphqlapi--examples--GraphQL_API_Creation_Example"></a>

The following example creates a GraphQL API\.

#### YAML<a name="aws-resource-appsync-graphqlapi--examples--GraphQL_API_Creation_Example--yaml"></a>

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
    Type: AWS::AppSync::GraphQLApi
    Properties:
      Name:
	Ref: graphQlApiName
      AuthenticationType: "AMAZON_COGNITO_USER_POOLS"
      UserPoolConfig:
        UserPoolId:
          Ref: userPoolId
        AwsRegion:
          Ref: userPoolAwsRegion
        DefaultAction:
          Ref: defaultAction
```

#### JSON<a name="aws-resource-appsync-graphqlapi--examples--GraphQL_API_Creation_Example--json"></a>

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
        "UserPoolConfig": {
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

## See also<a name="aws-resource-appsync-graphqlapi--seealso"></a>
+  [CreateGraphqlApi](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateGraphqlApi.html) operation in the *AWS AppSync API Reference*\.

