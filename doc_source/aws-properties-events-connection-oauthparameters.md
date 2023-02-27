# AWS::Events::Connection OAuthParameters<a name="aws-properties-events-connection-oauthparameters"></a>

Contains the OAuth authorization parameters to use for the connection\.

## Syntax<a name="aws-properties-events-connection-oauthparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-oauthparameters-syntax.json"></a>

```
{
  "[AuthorizationEndpoint](#cfn-events-connection-oauthparameters-authorizationendpoint)" : String,
  "[ClientParameters](#cfn-events-connection-oauthparameters-clientparameters)" : ClientParameters,
  "[HttpMethod](#cfn-events-connection-oauthparameters-httpmethod)" : String,
  "[OAuthHttpParameters](#cfn-events-connection-oauthparameters-oauthhttpparameters)" : ConnectionHttpParameters
}
```

### YAML<a name="aws-properties-events-connection-oauthparameters-syntax.yaml"></a>

```
  [AuthorizationEndpoint](#cfn-events-connection-oauthparameters-authorizationendpoint): String
  [ClientParameters](#cfn-events-connection-oauthparameters-clientparameters): 
    ClientParameters
  [HttpMethod](#cfn-events-connection-oauthparameters-httpmethod): String
  [OAuthHttpParameters](#cfn-events-connection-oauthparameters-oauthhttpparameters): 
    ConnectionHttpParameters
```

## Properties<a name="aws-properties-events-connection-oauthparameters-properties"></a>

`AuthorizationEndpoint`  <a name="cfn-events-connection-oauthparameters-authorizationendpoint"></a>
The URL to the authorization endpoint when OAuth is specified as the authorization type\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^((%[0-9A-Fa-f]{2}|[-()_.!~*';/?:@\x26=+$,A-Za-z0-9])+)([).!';/?:,])?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientParameters`  <a name="cfn-events-connection-oauthparameters-clientparameters"></a>
A `CreateConnectionOAuthClientRequestParameters` object that contains the client parameters for OAuth authorization\.  
*Required*: Yes  
*Type*: [ClientParameters](aws-properties-events-connection-clientparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-events-connection-oauthparameters-httpmethod"></a>
The method to use for the authorization request\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GET | POST | PUT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthHttpParameters`  <a name="cfn-events-connection-oauthparameters-oauthhttpparameters"></a>
A `ConnectionHttpParameters` object that contains details about the additional parameters to use for the connection\.  
*Required*: No  
*Type*: [ConnectionHttpParameters](aws-properties-events-connection-connectionhttpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)