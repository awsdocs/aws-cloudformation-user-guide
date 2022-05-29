# AWS::Events::Connection OAuthParameters<a name="aws-properties-events-connection-oauthparameters"></a>

<a name="aws-properties-events-connection-oauthparameters-description"></a>The `OAuthParameters` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::Events::Connection](aws-resource-events-connection.md)\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientParameters`  <a name="cfn-events-connection-oauthparameters-clientparameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [ClientParameters](aws-properties-events-connection-clientparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-events-connection-oauthparameters-httpmethod"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthHttpParameters`  <a name="cfn-events-connection-oauthparameters-oauthhttpparameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ConnectionHttpParameters](aws-properties-events-connection-connectionhttpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)