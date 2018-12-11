# Alexa::ASK::Skill AuthenticationConfiguration<a name="aws-properties-ask-skill-authenticationconfiguration"></a>

<a name="aws-properties-ask-skill-authenticationconfiguration-description"></a>The `AuthenticationConfiguration` property type specifies the Login with Amazon \(LWA\) configuration used to authenticate with the Alexa service\. Only Login with Amazon security profiles created through the [Amazon Developer Console](https://developer.amazon.com/lwa/sp/overview.html) are supported for authentication\. A Client ID, Client Secret, and Refresh Token are required\. You can generate a Client ID and Client Secret by creating a new [security profile](https://developer.amazon.com/lwa/sp/create-security-profile.html) on the Amazon Developer Portal or you can retrieve them from an existing profile\. You can then produce the refresh token by providing the Client ID and Client Secret to the [generate\-lwa\-tokens](https://developer.amazon.com/docs/smapi/ask-cli-command-reference.html#generate-lwa-tokens) command in the [ASK CLI](https://developer.amazon.com/docs/smapi/ask-cli-intro.html)\.

<a name="aws-properties-ask-skill-authenticationconfiguration-inheritance"></a> `AuthenticationConfiguration` is a property of the [Alexa::ASK::Skill](aws-resource-ask-skill.md) resource\.

## Syntax<a name="aws-properties-ask-skill-authenticationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ask-skill-authenticationconfiguration-syntax.json"></a>

```
{
  "[ClientId](#cfn-ask-skill-authenticationconfiguration-clientid)" : String,
  "[ClientSecret](#cfn-ask-skill-authenticationconfiguration-clientsecret)" : String,
  "[RefreshToken](#cfn-ask-skill-authenticationconfiguration-refreshtoken)" : String
}
```

### YAML<a name="aws-properties-ask-skill-authenticationconfiguration-syntax.yaml"></a>

```
[ClientId](#cfn-ask-skill-authenticationconfiguration-clientid): String
[ClientSecret](#cfn-ask-skill-authenticationconfiguration-clientsecret): String
[RefreshToken](#cfn-ask-skill-authenticationconfiguration-refreshtoken): String
```

## Properties<a name="aws-properties-ask-skill-authenticationconfiguration-properties"></a>

`ClientId`  <a name="cfn-ask-skill-authenticationconfiguration-clientid"></a>
Client ID from Login with Amazon \(LWA\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ClientSecret`  <a name="cfn-ask-skill-authenticationconfiguration-clientsecret"></a>
Client Secret from Login with Amazon \(LWA\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RefreshToken`  <a name="cfn-ask-skill-authenticationconfiguration-refreshtoken"></a>
Refresh Token from Login with Amazon \(LWA\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 