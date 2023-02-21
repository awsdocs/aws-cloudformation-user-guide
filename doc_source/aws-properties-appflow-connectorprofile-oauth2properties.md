# AWS::AppFlow::ConnectorProfile OAuth2Properties<a name="aws-properties-appflow-connectorprofile-oauth2properties"></a>

The OAuth 2\.0 properties required for OAuth 2\.0 authentication\.

## Syntax<a name="aws-properties-appflow-connectorprofile-oauth2properties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-oauth2properties-syntax.json"></a>

```
{
  "[OAuth2GrantType](#cfn-appflow-connectorprofile-oauth2properties-oauth2granttype)" : String,
  "[TokenUrl](#cfn-appflow-connectorprofile-oauth2properties-tokenurl)" : String,
  "[TokenUrlCustomProperties](#cfn-appflow-connectorprofile-oauth2properties-tokenurlcustomproperties)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-oauth2properties-syntax.yaml"></a>

```
  [OAuth2GrantType](#cfn-appflow-connectorprofile-oauth2properties-oauth2granttype): String
  [TokenUrl](#cfn-appflow-connectorprofile-oauth2properties-tokenurl): String
  [TokenUrlCustomProperties](#cfn-appflow-connectorprofile-oauth2properties-tokenurlcustomproperties): 
    Key : Value
```

## Properties<a name="aws-properties-appflow-connectorprofile-oauth2properties-properties"></a>

`OAuth2GrantType`  <a name="cfn-appflow-connectorprofile-oauth2properties-oauth2granttype"></a>
The OAuth 2\.0 grant type used by connector for OAuth 2\.0 authentication\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTHORIZATION_CODE | CLIENT_CREDENTIALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenUrl`  <a name="cfn-appflow-connectorprofile-oauth2properties-tokenurl"></a>
The token URL required for OAuth 2\.0 authentication\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^(https?)://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenUrlCustomProperties`  <a name="cfn-appflow-connectorprofile-oauth2properties-tokenurlcustomproperties"></a>
Associates your token URL with a map of properties that you define\. Use this parameter to provide any additional details that the connector requires to authenticate your request\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)