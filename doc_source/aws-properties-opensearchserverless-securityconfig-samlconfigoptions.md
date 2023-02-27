# AWS::OpenSearchServerless::SecurityConfig SamlConfigOptions<a name="aws-properties-opensearchserverless-securityconfig-samlconfigoptions"></a>

Describes SAML options for an OpenSearch Serverless security configuration in the form of a key\-value map\.

## Syntax<a name="aws-properties-opensearchserverless-securityconfig-samlconfigoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchserverless-securityconfig-samlconfigoptions-syntax.json"></a>

```
{
  "[GroupAttribute](#cfn-opensearchserverless-securityconfig-samlconfigoptions-groupattribute)" : String,
  "[Metadata](#cfn-opensearchserverless-securityconfig-samlconfigoptions-metadata)" : String,
  "[SessionTimeout](#cfn-opensearchserverless-securityconfig-samlconfigoptions-sessiontimeout)" : Integer,
  "[UserAttribute](#cfn-opensearchserverless-securityconfig-samlconfigoptions-userattribute)" : String
}
```

### YAML<a name="aws-properties-opensearchserverless-securityconfig-samlconfigoptions-syntax.yaml"></a>

```
  [GroupAttribute](#cfn-opensearchserverless-securityconfig-samlconfigoptions-groupattribute): String
  [Metadata](#cfn-opensearchserverless-securityconfig-samlconfigoptions-metadata): String
  [SessionTimeout](#cfn-opensearchserverless-securityconfig-samlconfigoptions-sessiontimeout): Integer
  [UserAttribute](#cfn-opensearchserverless-securityconfig-samlconfigoptions-userattribute): String
```

## Properties<a name="aws-properties-opensearchserverless-securityconfig-samlconfigoptions-properties"></a>

`GroupAttribute`  <a name="cfn-opensearchserverless-securityconfig-samlconfigoptions-groupattribute"></a>
The group attribute for this SAML integration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metadata`  <a name="cfn-opensearchserverless-securityconfig-samlconfigoptions-metadata"></a>
The XML IdP metadata file generated from your identity provider\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionTimeout`  <a name="cfn-opensearchserverless-securityconfig-samlconfigoptions-sessiontimeout"></a>
The session timeout, in minutes\. Default is 60 minutes \(12 hours\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserAttribute`  <a name="cfn-opensearchserverless-securityconfig-samlconfigoptions-userattribute"></a>
A user attribute for this SAML integration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)