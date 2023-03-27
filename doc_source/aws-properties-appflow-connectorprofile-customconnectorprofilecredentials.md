# AWS::AppFlow::ConnectorProfile CustomConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-customconnectorprofilecredentials"></a>

The connector\-specific profile credentials that are required when using the custom connector\.

## Syntax<a name="aws-properties-appflow-connectorprofile-customconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-customconnectorprofilecredentials-syntax.json"></a>

```
{
  "[ApiKey](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-apikey)" : ApiKeyCredentials,
  "[AuthenticationType](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-authenticationtype)" : String,
  "[Basic](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-basic)" : BasicAuthCredentials,
  "[Custom](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-custom)" : CustomAuthCredentials,
  "[Oauth2](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-oauth2)" : OAuth2Credentials
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-customconnectorprofilecredentials-syntax.yaml"></a>

```
  [ApiKey](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-apikey): 
    ApiKeyCredentials
  [AuthenticationType](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-authenticationtype): String
  [Basic](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-basic): 
    BasicAuthCredentials
  [Custom](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-custom): 
    CustomAuthCredentials
  [Oauth2](#cfn-appflow-connectorprofile-customconnectorprofilecredentials-oauth2): 
    OAuth2Credentials
```

## Properties<a name="aws-properties-appflow-connectorprofile-customconnectorprofilecredentials-properties"></a>

`ApiKey`  <a name="cfn-appflow-connectorprofile-customconnectorprofilecredentials-apikey"></a>
The API keys required for the authentication of the user\.  
*Required*: No  
*Type*: [ApiKeyCredentials](aws-properties-appflow-connectorprofile-apikeycredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthenticationType`  <a name="cfn-appflow-connectorprofile-customconnectorprofilecredentials-authenticationtype"></a>
The authentication type that the custom connector uses for authenticating while creating a connector profile\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `APIKEY | BASIC | CUSTOM | OAUTH2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Basic`  <a name="cfn-appflow-connectorprofile-customconnectorprofilecredentials-basic"></a>
The basic credentials that are required for the authentication of the user\.  
*Required*: No  
*Type*: [BasicAuthCredentials](aws-properties-appflow-connectorprofile-basicauthcredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Custom`  <a name="cfn-appflow-connectorprofile-customconnectorprofilecredentials-custom"></a>
If the connector uses the custom authentication mechanism, this holds the required credentials\.  
*Required*: No  
*Type*: [CustomAuthCredentials](aws-properties-appflow-connectorprofile-customauthcredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Oauth2`  <a name="cfn-appflow-connectorprofile-customconnectorprofilecredentials-oauth2"></a>
The OAuth 2\.0 credentials required for the authentication of the user\.  
*Required*: No  
*Type*: [OAuth2Credentials](aws-properties-appflow-connectorprofile-oauth2credentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)