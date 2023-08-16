# AWS::AppFlow::ConnectorProfile OAuthProperties<a name="aws-properties-appflow-connectorprofile-oauthproperties"></a>

 The OAuth properties required for OAuth type authentication\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-oauthproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-oauthproperties-syntax.json"></a>

```
{
  "[AuthCodeUrl](#cfn-appflow-connectorprofile-oauthproperties-authcodeurl)" : String,
  "[OAuthScopes](#cfn-appflow-connectorprofile-oauthproperties-oauthscopes)" : [ String, ... ],
  "[TokenUrl](#cfn-appflow-connectorprofile-oauthproperties-tokenurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-oauthproperties-syntax.yaml"></a>

```
  [AuthCodeUrl](#cfn-appflow-connectorprofile-oauthproperties-authcodeurl): String
  [OAuthScopes](#cfn-appflow-connectorprofile-oauthproperties-oauthscopes): 
    - String
  [TokenUrl](#cfn-appflow-connectorprofile-oauthproperties-tokenurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-oauthproperties-properties"></a>

`AuthCodeUrl`  <a name="cfn-appflow-connectorprofile-oauthproperties-authcodeurl"></a>
 The authorization code url required to redirect to SAP Login Page to fetch authorization code for OAuth type authentication\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^(https?)://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthScopes`  <a name="cfn-appflow-connectorprofile-oauthproperties-oauthscopes"></a>
 The OAuth scopes required for OAuth type authentication\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenUrl`  <a name="cfn-appflow-connectorprofile-oauthproperties-tokenurl"></a>
 The token url required to fetch access/refresh tokens using authorization code and also to refresh expired access token using refresh token\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^(https?)://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)