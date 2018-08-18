# AWS AppSync GraphQLApi OpenId Connect Config<a name="aws-properties-appsync-graphqlapi-openidconnectconfig"></a>

<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-description"></a>The `OpenIDConnectConfig` property type specifies the optional authorization configuration for using an Open Id Connect compliant service with your GraphQL endpoint for an AWS AppSync GraphQL API\.

<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-inheritance"></a> `OpenIDConnectConfig` is a property of the [AWS::AppSync::GraphQLApi](aws-resource-appsync-graphqlapi.md) property type\.

## Syntax<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-syntax.json"></a>

```
{
  "[Issuer](#cfn-appsync-graphqlapi-openidconnectconfig-issuer)" : String,
  "[ClientId](#cfn-appsync-graphqlapi-openidconnectconfig-clientid)" : String,
  "[IatTTL](#cfn-appsync-graphqlapi-openidconnectconfig-iatttl)" : Number,
  "[AuthTTL](#cfn-appsync-graphqlapi-openidconnectconfig-authttl)" : Number
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-syntax.yaml"></a>

```
[Issuer](#cfn-appsync-graphqlapi-openidconnectconfig-issuer): String
[ClientId](#cfn-appsync-graphqlapi-openidconnectconfig-clientid): String
[IatTTL](#cfn-appsync-graphqlapi-openidconnectconfig-iatttl): Number
[AuthTTL](#cfn-appsync-graphqlapi-openidconnectconfig-authttl): Number
```

## Properties<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-properties"></a>

`Issuer`  <a name="cfn-appsync-graphqlapi-openidconnectconfig-issuer"></a>
The issuer for the open id connect configuration\. The issuer returned by discovery MUST exactly match the value of iss in the ID Token\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ClientId`  <a name="cfn-appsync-graphqlapi-openidconnectconfig-clientid"></a>
The client identifier of the Relying party at the OpenID Provider\. This identifier is typically obtained when the Relying party is registered with the OpenID Provider\. You can specify a regular expression so the AWS AppSync can validate against multiple client identifiers at a time  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IatTTL`  <a name="cfn-appsync-graphqlapi-openidconnectconfig-iatttl"></a>
The number of milliseconds a token is valid after being issued to a user\.  
 *Required*: No  
 *Type*: Number  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthTTL`  <a name="cfn-appsync-graphqlapi-openidconnectconfig-authttl"></a>
The number of milliseconds a token is valid after being authenticated\.  
 *Required*: No  
 *Type*: Number  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-graphqlapi-openidconnectconfig-seealso"></a>
+ [ OpenIDConnectConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_OpenIDConnectConfig.html) operation in the *AWS AppSync API Reference*