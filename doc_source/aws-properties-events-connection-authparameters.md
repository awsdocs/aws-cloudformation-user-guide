# AWS::Events::Connection AuthParameters<a name="aws-properties-events-connection-authparameters"></a>

Contains the authorization parameters to use for the connection\.

## Syntax<a name="aws-properties-events-connection-authparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-authparameters-syntax.json"></a>

```
{
  "[ApiKeyAuthParameters](#cfn-events-connection-authparameters-apikeyauthparameters)" : ApiKeyAuthParameters,
  "[BasicAuthParameters](#cfn-events-connection-authparameters-basicauthparameters)" : BasicAuthParameters,
  "[InvocationHttpParameters](#cfn-events-connection-authparameters-invocationhttpparameters)" : ConnectionHttpParameters,
  "[OAuthParameters](#cfn-events-connection-authparameters-oauthparameters)" : OAuthParameters
}
```

### YAML<a name="aws-properties-events-connection-authparameters-syntax.yaml"></a>

```
  [ApiKeyAuthParameters](#cfn-events-connection-authparameters-apikeyauthparameters): 
    ApiKeyAuthParameters
  [BasicAuthParameters](#cfn-events-connection-authparameters-basicauthparameters): 
    BasicAuthParameters
  [InvocationHttpParameters](#cfn-events-connection-authparameters-invocationhttpparameters): 
    ConnectionHttpParameters
  [OAuthParameters](#cfn-events-connection-authparameters-oauthparameters): 
    OAuthParameters
```

## Properties<a name="aws-properties-events-connection-authparameters-properties"></a>

`ApiKeyAuthParameters`  <a name="cfn-events-connection-authparameters-apikeyauthparameters"></a>
The API Key parameters to use for authorization\.  
*Required*: No  
*Type*: [ApiKeyAuthParameters](aws-properties-events-connection-apikeyauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasicAuthParameters`  <a name="cfn-events-connection-authparameters-basicauthparameters"></a>
The authorization parameters for Basic authorization\.  
*Required*: No  
*Type*: [BasicAuthParameters](aws-properties-events-connection-basicauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationHttpParameters`  <a name="cfn-events-connection-authparameters-invocationhttpparameters"></a>
Additional parameters for the connection that are passed through with every invocation to the HTTP endpoint\.  
*Required*: No  
*Type*: [ConnectionHttpParameters](aws-properties-events-connection-connectionhttpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthParameters`  <a name="cfn-events-connection-authparameters-oauthparameters"></a>
The OAuth parameters to use for authorization\.  
*Required*: No  
*Type*: [OAuthParameters](aws-properties-events-connection-oauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)