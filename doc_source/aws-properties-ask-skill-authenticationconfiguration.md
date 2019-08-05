# Alexa::ASK::Skill AuthenticationConfiguration<a name="aws-properties-ask-skill-authenticationconfiguration"></a>

The `AuthenticationConfiguration` property type specifies the Login with Amazon \(LWA\) configuration used to authenticate with the Alexa service\. Only Login with Amazon security profiles created through the [Amazon Developer Console](https://developer.amazon.com/lwa/sp/overview.html) are supported for authentication\. A client ID, client secret, and refresh token are required\. You can generate a client ID and client secret by creating a new [security profile](https://developer.amazon.com/lwa/sp/create-security-profile.html) on the Amazon Developer Portal or you can retrieve them from an existing profile\. You can then produce the refresh token by providing the client ID and client secret to the [generate\-lwa\-tokens](https://developer.amazon.com/docs/smapi/ask-cli-command-reference.html#generate-lwa-tokens) command in the [ASK CLI](https://developer.amazon.com/docs/smapi/ask-cli-intro.html)\.

 `AuthenticationConfiguration` is a property of the `Alexa::ASK::Skill` resource\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-ask-skill-authenticationconfiguration-clientsecret"></a>
Client secret from Login with Amazon \(LWA\)\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshToken`  <a name="cfn-ask-skill-authenticationconfiguration-refreshtoken"></a>
Refresh token from Login with Amazon \(LWA\)\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
