# AWS::Cognito::IdentityPoolPrincipalTag<a name="aws-resource-cognito-identitypoolprincipaltag"></a>

A list of the identity pool principal tag assignments for attributes for access control\.

## Syntax<a name="aws-resource-cognito-identitypoolprincipaltag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypoolprincipaltag-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPoolPrincipalTag",
  "Properties" : {
      "[IdentityPoolId](#cfn-cognito-identitypoolprincipaltag-identitypoolid)" : String,
      "[IdentityProviderName](#cfn-cognito-identitypoolprincipaltag-identityprovidername)" : String,
      "[PrincipalTags](#cfn-cognito-identitypoolprincipaltag-principaltags)" : Json,
      "[UseDefaults](#cfn-cognito-identitypoolprincipaltag-usedefaults)" : Boolean
    }
}
```

### YAML<a name="aws-resource-cognito-identitypoolprincipaltag-syntax.yaml"></a>

```
Type: AWS::Cognito::IdentityPoolPrincipalTag
Properties: 
  [IdentityPoolId](#cfn-cognito-identitypoolprincipaltag-identitypoolid): String
  [IdentityProviderName](#cfn-cognito-identitypoolprincipaltag-identityprovidername): String
  [PrincipalTags](#cfn-cognito-identitypoolprincipaltag-principaltags): Json
  [UseDefaults](#cfn-cognito-identitypoolprincipaltag-usedefaults): Boolean
```

## Properties<a name="aws-resource-cognito-identitypoolprincipaltag-properties"></a>

`IdentityPoolId`  <a name="cfn-cognito-identitypoolprincipaltag-identitypoolid"></a>
The identity pool that you want to associate with this principal tag map\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdentityProviderName`  <a name="cfn-cognito-identitypoolprincipaltag-identityprovidername"></a>
The identity pool identity provider \(IdP\) that you want to associate with this principal tag map\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalTags`  <a name="cfn-cognito-identitypoolprincipaltag-principaltags"></a>
A JSON\-formatted list of user claims and the principal tags that you want to associate with them\. When Amazon Cognito requests credentials, it sets the value of the principal tag to the value of the user's claim\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseDefaults`  <a name="cfn-cognito-identitypoolprincipaltag-usedefaults"></a>
Use a default set of mappings between claims and tags for this provider, instead of a custom map\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cognito-identitypoolprincipaltag-return-values"></a>

### Ref<a name="aws-resource-cognito-identitypoolprincipaltag-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the principal tag primary ID, like `us-east-1:1cf667a2-49a6-454b-9e45-23199EXAMPLE|graph.facebook.com`\.

## Examples<a name="aws-resource-cognito-identitypoolprincipaltag--examples"></a>



### Creating a new principal tag attribute map for an identity pool<a name="aws-resource-cognito-identitypoolprincipaltag--examples--Creating_a_new_principal_tag_attribute_map_for_an_identity_pool"></a>

The following example maps the claim `aud` to principal tag `app_id` and the claim `sub` to `user_id` in the identity pool `Example_pool.`

#### YAML<a name="aws-resource-cognito-identitypoolprincipaltag--examples--Creating_a_new_principal_tag_attribute_map_for_an_identity_pool--yaml"></a>

```
  AWSTemplateFormatVersion: "2010-09-09"
  Description: Cognito Principal Tags Example  
  Resources:
    ExamplePool: 
      Type: AWS::Cognito::IdentityPool
        Properties:
          IdentityPoolName: 'example_pool'
          AllowUnauthenticatedIdentities: True      
          SupportedLoginProviders:
            "graph.facebook.com": "abcdExampleClientId"
    PrincipalTags:
      Type: AWS::Cognito::IdentityPoolPrincipalTag
        Properties:
          IdentityPoolId: !Ref 'ExamplePool'
          IdentityProviderName: "graph.facebook.com"
          PrincipalTags:                 
            app_id: "aud"
            user_id: "sub"
          UseDefaults: false
```