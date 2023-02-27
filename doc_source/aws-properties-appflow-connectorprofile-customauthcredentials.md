# AWS::AppFlow::ConnectorProfile CustomAuthCredentials<a name="aws-properties-appflow-connectorprofile-customauthcredentials"></a>

The custom credentials required for custom authentication\.

## Syntax<a name="aws-properties-appflow-connectorprofile-customauthcredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-customauthcredentials-syntax.json"></a>

```
{
  "[CredentialsMap](#cfn-appflow-connectorprofile-customauthcredentials-credentialsmap)" : {Key : Value, ...},
  "[CustomAuthenticationType](#cfn-appflow-connectorprofile-customauthcredentials-customauthenticationtype)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-customauthcredentials-syntax.yaml"></a>

```
  [CredentialsMap](#cfn-appflow-connectorprofile-customauthcredentials-credentialsmap): 
    Key : Value
  [CustomAuthenticationType](#cfn-appflow-connectorprofile-customauthcredentials-customauthenticationtype): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-customauthcredentials-properties"></a>

`CredentialsMap`  <a name="cfn-appflow-connectorprofile-customauthcredentials-credentialsmap"></a>
A map that holds custom authentication credentials\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomAuthenticationType`  <a name="cfn-appflow-connectorprofile-customauthcredentials-customauthenticationtype"></a>
The custom authentication type that the connector uses\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)