# AWS::Events::Connection AuthParameters<a name="aws-properties-events-connection-authparameters"></a>

Contains the authorization parameters to use to authorize with the endpoint\. 

## Syntax<a name="aws-properties-events-connection-authparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-authparameters-syntax.json"></a>

```
{
  "[ApiKeyAuthParameters](#cfn-events-connection-authparameters-apikeyauthparameters)" : ApiKeyAuthParameters,
  "[BasicAuthParameters](#cfn-events-connection-authparameters-basicauthparameters)" : BasicAuthParameters,
  "[InvocationHttpParameters](#cfn-events-connection-authparameters-invocationhttpparameters)" : HttpParameters,
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
    HttpParameters
  [OAuthParameters](#cfn-events-connection-authparameters-oauthparameters): 
    OAuthParameters
```

## Properties<a name="aws-properties-events-connection-authparameters-properties"></a>

`ApiKeyAuthParameters`  <a name="cfn-events-connection-authparameters-apikeyauthparameters"></a>
Contains the API key authorization parameters to use for the connection\.   
*Required*: No  
*Type*: [ApiKeyAuthParameters](aws-properties-events-connection-apikeyauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasicAuthParameters`  <a name="cfn-events-connection-authparameters-basicauthparameters"></a>
Contains the Basic authorization parameters to use for the connection\.   
*Required*: No  
*Type*: [BasicAuthParameters](aws-properties-events-connection-basicauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationHttpParameters`  <a name="cfn-events-connection-authparameters-invocationhttpparameters"></a>
Contains the API key authorization parameters to use for the connection\. Note that if you include additional parameters for the target of a rule via HttpParameters, including query strings, the parameters added for the connection take precedence\.   
*Required*: No  
*Type*: [HttpParameters](aws-properties-events-connection-httpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthParameters`  <a name="cfn-events-connection-authparameters-oauthparameters"></a>
Contains the OAuth authorization parameters to use for the connection\.  
*Required*: No  
*Type*: [OAuthParameters](aws-properties-events-connection-oauthparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)