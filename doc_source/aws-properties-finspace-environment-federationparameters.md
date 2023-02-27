# AWS::FinSpace::Environment FederationParameters<a name="aws-properties-finspace-environment-federationparameters"></a>

Configuration information when authentication mode is FEDERATED\.

## Syntax<a name="aws-properties-finspace-environment-federationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-finspace-environment-federationparameters-syntax.json"></a>

```
{
  "[ApplicationCallBackURL](#cfn-finspace-environment-federationparameters-applicationcallbackurl)" : String,
  "[AttributeMap](#cfn-finspace-environment-federationparameters-attributemap)" : Json,
  "[FederationProviderName](#cfn-finspace-environment-federationparameters-federationprovidername)" : String,
  "[FederationURN](#cfn-finspace-environment-federationparameters-federationurn)" : String,
  "[SamlMetadataDocument](#cfn-finspace-environment-federationparameters-samlmetadatadocument)" : String,
  "[SamlMetadataURL](#cfn-finspace-environment-federationparameters-samlmetadataurl)" : String
}
```

### YAML<a name="aws-properties-finspace-environment-federationparameters-syntax.yaml"></a>

```
  [ApplicationCallBackURL](#cfn-finspace-environment-federationparameters-applicationcallbackurl): String
  [AttributeMap](#cfn-finspace-environment-federationparameters-attributemap): Json
  [FederationProviderName](#cfn-finspace-environment-federationparameters-federationprovidername): String
  [FederationURN](#cfn-finspace-environment-federationparameters-federationurn): String
  [SamlMetadataDocument](#cfn-finspace-environment-federationparameters-samlmetadatadocument): String
  [SamlMetadataURL](#cfn-finspace-environment-federationparameters-samlmetadataurl): String
```

## Properties<a name="aws-properties-finspace-environment-federationparameters-properties"></a>

`ApplicationCallBackURL`  <a name="cfn-finspace-environment-federationparameters-applicationcallbackurl"></a>
The redirect or sign\-in URL that should be entered into the SAML 2\.0 compliant identity provider configuration \(IdP\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `^https?://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributeMap`  <a name="cfn-finspace-environment-federationparameters-attributemap"></a>
SAML attribute name and value\. The name must always be `Email` and the value should be set to the attribute definition in which user email is set\. For example, name would be `Email` and value `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress`\. Please check your SAML 2\.0 compliant identity provider \(IdP\) documentation for details\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FederationProviderName`  <a name="cfn-finspace-environment-federationparameters-federationprovidername"></a>
Name of the identity provider \(IdP\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[^_\p{Z}][\p{L}\p{M}\p{S}\p{N}\p{P}][^_\p{Z}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FederationURN`  <a name="cfn-finspace-environment-federationparameters-federationurn"></a>
The Uniform Resource Name \(URN\)\. Also referred as Service Provider URN or Audience URI or Service Provider Entity ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[A-Za-z0-9._\-:\/#\+]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamlMetadataDocument`  <a name="cfn-finspace-environment-federationparameters-samlmetadatadocument"></a>
SAML 2\.0 Metadata document from identity provider \(IdP\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1000`  
*Maximum*: `10000000`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamlMetadataURL`  <a name="cfn-finspace-environment-federationparameters-samlmetadataurl"></a>
Provide the metadata URL from your SAML 2\.0 compliant identity provider \(IdP\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `^https?://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)