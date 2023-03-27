# AWS::OpenSearchServerless::SecurityConfig<a name="aws-resource-opensearchserverless-securityconfig"></a>

Specifies a security configuration for OpenSearch Serverless\. For more information, see [SAML authentication for Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-saml.html)\. 

## Syntax<a name="aws-resource-opensearchserverless-securityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchserverless-securityconfig-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchServerless::SecurityConfig",
  "Properties" : {
      "[Description](#cfn-opensearchserverless-securityconfig-description)" : String,
      "[Name](#cfn-opensearchserverless-securityconfig-name)" : String,
      "[SamlOptions](#cfn-opensearchserverless-securityconfig-samloptions)" : SamlConfigOptions,
      "[Type](#cfn-opensearchserverless-securityconfig-type)" : String
    }
}
```

### YAML<a name="aws-resource-opensearchserverless-securityconfig-syntax.yaml"></a>

```
Type: AWS::OpenSearchServerless::SecurityConfig
Properties: 
  [Description](#cfn-opensearchserverless-securityconfig-description): String
  [Name](#cfn-opensearchserverless-securityconfig-name): String
  [SamlOptions](#cfn-opensearchserverless-securityconfig-samloptions): 
    SamlConfigOptions
  [Type](#cfn-opensearchserverless-securityconfig-type): String
```

## Properties<a name="aws-resource-opensearchserverless-securityconfig-properties"></a>

`Description`  <a name="cfn-opensearchserverless-securityconfig-description"></a>
The description of the security configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opensearchserverless-securityconfig-name"></a>
The name of the security configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SamlOptions`  <a name="cfn-opensearchserverless-securityconfig-samloptions"></a>
SAML options for the security configuration in the form of a key\-value map\.  
*Required*: No  
*Type*: [SamlConfigOptions](aws-properties-opensearchserverless-securityconfig-samlconfigoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opensearchserverless-securityconfig-type"></a>
The type of security configuration\. Currently the only option is `saml`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opensearchserverless-securityconfig-return-values"></a>

### Ref<a name="aws-resource-opensearchserverless-securityconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the ID of the security configuration\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opensearchserverless-securityconfig-return-values-fn--getatt"></a>

`GetAtt` returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-opensearchserverless-securityconfig-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier of the security configuration\. For example, `saml/123456789012/myprovider`\.

## Examples<a name="aws-resource-opensearchserverless-securityconfig--examples"></a>

### Create a security configuration that specifies a YAML provider<a name="aws-resource-opensearchserverless-securityconfig--examples--Create_a_security_configuration_that_specifies_a_YAML_provider"></a>

The following example specifies an OpenSearch Serverless SAML provider named `my-provider` with a custom group attribute `ALLGroups`\.

#### JSON<a name="aws-resource-opensearchserverless-securityconfig--examples--Create_a_security_configuration_that_specifies_a_YAML_provider--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "OpenSearch Serverless security policy template",
  "Resources": {
    "TestSecurityConfig": {
      "Type": "AWS::OpenSearchServerless::SecurityConfig",
      "Properties": {
        "Name": "my-provider",
        "Type": "saml",
        "Description": "Serverless SAML configuration",
        "SamlOptions": {
          "Metadata": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><md:EntityDescriptor entityID=\"http://www.okta.com/foobar\" xmlns:md=\"urn:oasis:names:tc:SAML:2.0:metadata\"><md:IDPSSODescriptor WantAuthnRequestsSigned=\"false\" protocolSupportEnumeration=\"urn:oasis:names:tc:SAML:2.0:protocol\"><md:KeyDescriptor use=\"signing\"><ds:KeyInfo xmlns:ds=\"http://www.w3.org/2000/09/xmldsig#\"><ds:X509Data><ds:X509Certificate>Mfoobar</ds:X509Certificate></ds:X509Data></ds:KeyInfo></md:KeyDescriptor><md:NameIDFormat>urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress</md:NameIDFormat><md:SingleSignOnService Binding=\"urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST\" Location=\"https://trial-1234567.okta.com/app/trial-1234567_saml2_1/foobar/sso/saml\"/><md:SingleSignOnService Binding=\"urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect\" Location=\"https://trial-1234567.okta.com/app/trial-1234567_saml2_1/foobar/sso/saml\"/></md:IDPSSODescriptor></md:EntityDescriptor>",
          "UserAttribute": "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier",
          "GroupAttribute": "ALLGroups",
          "SessionTimeout": 120
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-opensearchserverless-securityconfig--examples--Create_a_security_configuration_that_specifies_a_YAML_provider--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless security policy template'
Resources:
  TestSecurityConfig:
    Type: 'AWS::OpenSearchServerless::SecurityConfig'
    Properties:
      Name: my-provider
      Type: saml
      Description: Serverless SAML configuration
      SamlOptions:
        Metadata: >-
          <?xml version="1.0" encoding="UTF-8"?><md:EntityDescriptor
          entityID="http://www.okta.com/foobar"
          xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata"><md:IDPSSODescriptor
          WantAuthnRequestsSigned="false"
          protocolSupportEnumeration="urn:oasis:names:tc:SAML:2.0:protocol"><md:KeyDescriptor
          use="signing"><ds:KeyInfo
          xmlns:ds="http://www.w3.org/2000/09/xmldsig#"><ds:X509Data><ds:X509Certificate>Mfoobar</ds:X509Certificate></ds:X509Data></ds:KeyInfo></md:KeyDescriptor><md:NameIDFormat>urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress</md:NameIDFormat><md:SingleSignOnService
          Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST"
          Location="https://trial-1234567.okta.com/app/trial-1234567_saml2_1/foobar/sso/saml"/><md:SingleSignOnService
          Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect"
          Location="https://trial-1234567.okta.com/app/trial-1234567_saml2_1/foobar/sso/saml"/></md:IDPSSODescriptor></md:EntityDescriptor>
        UserAttribute: 'http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier'
        GroupAttribute: ALLGroups
        SessionTimeout: 120
```