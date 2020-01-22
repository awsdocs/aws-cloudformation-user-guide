# AWS::Cognito::UserPoolIdentityProvider<a name="aws-resource-cognito-userpoolidentityprovider"></a>

The `AWS::Cognito::UserPoolIdentityProvider` resource creates an identity provider for a user pool\.

## Syntax<a name="aws-resource-cognito-userpoolidentityprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolidentityprovider-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolIdentityProvider",
  "Properties" : {
      "[AttributeMapping](#cfn-cognito-userpoolidentityprovider-attributemapping)" : Json,
      "[IdpIdentifiers](#cfn-cognito-userpoolidentityprovider-idpidentifiers)" : [ String, ... ],
      "[ProviderDetails](#cfn-cognito-userpoolidentityprovider-providerdetails)" : Json,
      "[ProviderName](#cfn-cognito-userpoolidentityprovider-providername)" : String,
      "[ProviderType](#cfn-cognito-userpoolidentityprovider-providertype)" : String,
      "[UserPoolId](#cfn-cognito-userpoolidentityprovider-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolidentityprovider-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolIdentityProvider
Properties: 
  [AttributeMapping](#cfn-cognito-userpoolidentityprovider-attributemapping): Json
  [IdpIdentifiers](#cfn-cognito-userpoolidentityprovider-idpidentifiers): 
    - String
  [ProviderDetails](#cfn-cognito-userpoolidentityprovider-providerdetails): Json
  [ProviderName](#cfn-cognito-userpoolidentityprovider-providername): String
  [ProviderType](#cfn-cognito-userpoolidentityprovider-providertype): String
  [UserPoolId](#cfn-cognito-userpoolidentityprovider-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpoolidentityprovider-properties"></a>

`AttributeMapping`  <a name="cfn-cognito-userpoolidentityprovider-attributemapping"></a>
A mapping of identity provider attributes to standard and custom user pool attributes\. Available user pool attributes shall be formatted in snake_case, i.e. "FamilyName" user pool attribute shall be referenced as "family_name" in AttributeMapping JSON\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdpIdentifiers`  <a name="cfn-cognito-userpoolidentityprovider-idpidentifiers"></a>
A list of identity provider identifiers\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProviderDetails`  <a name="cfn-cognito-userpoolidentityprovider-providerdetails"></a>
The identity provider details, such as `MetadataURL` and `MetadataFile`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProviderName`  <a name="cfn-cognito-userpoolidentityprovider-providername"></a>
The identity provider name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[^_][\p{L}\p{M}\p{S}\p{N}\p{P}][^_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProviderType`  <a name="cfn-cognito-userpoolidentityprovider-providertype"></a>
The identity provider type\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `Facebook | Google | LoginWithAmazon | OIDC | SAML | SignInWithApple`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpoolidentityprovider-userpoolid"></a>
The user pool ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-cognito-userpoolidentityprovider-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolidentityprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns physicalResourceId, which is “ProviderName"\. For example:

 `{ "Ref": "testProvider" }` 

For the Amazon Cognito identity provider `testProvider`, Ref returns the name of the identity provider\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpoolidentityprovider--examples"></a>

### Creating a new identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_identity_provider"></a>

The following example creates the identity provider "YourProviderName" in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_identity_provider--json"></a>

```
{
      "UserPoolIdentityProvider": {
          "Type": "AWS::Cognito::UserPoolIdentityProvider",
          "Properties": {
               "UserPoolId": {"Ref": "UserPool"},
               "ProviderName": "YourProviderName",
               "ProviderDetails": {
                   "MetadataURL": "YourMetadataURL"
              },
              "ProviderType": "SAML",
              "AttributeMapping": {
                  "email": "Attribute",
                  "family_name": "Attribute"
               },
               "IdpIdentifiers": [
                    "IdpIdentifier"
                ]
             }
         }
     }
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_identity_provider--yaml"></a>

```
UserPoolIdentityProvider: 
        Type: AWS::Cognito::UserPoolIdentityProvider
        Properties:
            UserPoolId: !Ref UserPool
            ProviderName: "YourProviderName"
            ProviderDetails:
              MetadataURL: "YourMetadataURL"
            ProviderType: "SAML"
            AttributeMapping:
                email: "Attribute"
                family_name: "Attribute"
             IdpIdentifiers:
                - "IdpIdentifier"
```