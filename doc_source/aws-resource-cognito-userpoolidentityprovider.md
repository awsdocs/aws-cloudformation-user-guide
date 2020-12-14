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
A mapping of identity provider attributes to standard and custom user pool attributes\.  
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
The identity provider details\. The following list describes the provider detail keys for each identity provider type\.  
+ For Google and Login with Amazon:
  + client\_id
  + client\_secret
  + authorize\_scopes
+ For Facebook:
  + client\_id
  + client\_secret
  + authorize\_scopes
  + api\_version
+ For Sign in with Apple:
  + client\_id
  + team\_id
  + key\_id
  + private\_key
  + authorize\_scopes
+ For OIDC providers:
  + client\_id
  + client\_secret
  + attributes\_request\_method
  + oidc\_issuer
  + authorize\_scopes
  + authorize\_url *if not available from discovery URL specified by oidc\_issuer key* 
  + token\_url *if not available from discovery URL specified by oidc\_issuer key* 
  + attributes\_url *if not available from discovery URL specified by oidc\_issuer key* 
  + jwks\_uri *if not available from discovery URL specified by oidc\_issuer key* 
+ For SAML providers:
  + MetadataFile OR MetadataURL
  + IDPSignout *optional* 
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
*Allowed values*: `Facebook | Google | LoginWithAmazon | OIDC | SAML | SignInWithApple`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserPoolId`  <a name="cfn-cognito-userpoolidentityprovider-userpoolid"></a>
The user pool ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpoolidentityprovider-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolidentityprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns physicalResourceId, which is “ProviderName"\. For example:

 `{ "Ref": "testProvider" }` 

For the Amazon Cognito identity provider `testProvider`, Ref returns the name of the identity provider\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpoolidentityprovider--examples"></a>



### Creating a new Login with Amazon identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Login_with_Amazon_identity_provider"></a>

The following example creates a Login with Amazon identity provider in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Login_with_Amazon_identity_provider--json"></a>

```
{
  "UserPoolIdentityProvider": {
    "Type": "AWS::Cognito::UserPoolIdentityProvider",
    "Properties": {
      "UserPoolId": {
        "Ref": "UserPool"
      },
      "ProviderName": "LoginWithAmazon",
      "ProviderDetails": {
        "client_id": "YourLoginWithAmazonAppId",
        "client_secret": "YourLoginWithAmazonAppSecret",
        "authorize_scopes": "profile postal_code"
      },
      "ProviderType": "LoginWithAmazon",
      "AttributeMapping": {
        "email": "email"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Login_with_Amazon_identity_provider--yaml"></a>

```
UserPoolIdentityProvider:
  Type: AWS::Cognito::UserPoolIdentityProvider
  Properties:
    UserPoolId: !Ref UserPool
    ProviderName: "LoginWithAmazon"
    ProviderDetails:
      client_id: "YourLoginWithAmazonAppId"
      client_secret: "YourLoginWithAmazonAppSecret"
      authorize_scopes: "profile postal_code"
    ProviderType: "LoginWithAmazon"
    AttributeMapping:
      email: "email"
```

### Creating a new Google identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Google_identity_provider"></a>

The following example creates a Google identity provider in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Google_identity_provider--json"></a>

```
{
  "UserPoolIdentityProvider": {
    "Type": "AWS::Cognito::UserPoolIdentityProvider",
    "Properties": {
      "UserPoolId": {
        "Ref": "UserPool"
      },
      "ProviderName": "Google",
      "ProviderDetails": {
        "client_id": "YourGoogleAppId",
        "client_secret": "YourGoogleAppSecret",
        "authorize_scopes": "profile email openid"
      },
      "ProviderType": "Google",
      "AttributeMapping": {
        "email": "email"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Google_identity_provider--yaml"></a>

```
UserPoolIdentityProvider:
  Type: AWS::Cognito::UserPoolIdentityProvider
  Properties:
    UserPoolId: !Ref UserPool
    ProviderName: "Google"
    ProviderDetails:
      client_id: "YourGoogleAppId"
      client_secret: "YourGoogleAppSecret"
      authorize_scopes: "profile email openid"
    ProviderType: "Google"
    AttributeMapping:
      email: "email"
```

### Creating a new Facebook identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Facebook_identity_provider"></a>

The following example creates a Facebook identity provider in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Facebook_identity_provider--json"></a>

```
{
  "UserPoolIdentityProvider": {
    "Type": "AWS::Cognito::UserPoolIdentityProvider",
    "Properties": {
      "UserPoolId": {
        "Ref": "UserPool"
      },
      "ProviderName": "Facebook",
      "ProviderDetails": {
        "client_id": "YourFacebookAppId",
        "client_secret": "YourFacebookAppSecret",
        "authorize_scopes": "public_profile,email"
      },
      "ProviderType": "Facebook",
      "AttributeMapping": {
        "email": "email"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Facebook_identity_provider--yaml"></a>

```
UserPoolIdentityProvider:
  Type: AWS::Cognito::UserPoolIdentityProvider
  Properties:
    UserPoolId: !Ref UserPool
    ProviderName: "Facebook"
    ProviderDetails:
      client_id: "YourFacebookAppId"
      client_secret: "YourFacebookAppSecret"
      authorize_scopes: "public_profile,email"
    ProviderType: "Facebook"
    AttributeMapping:
      email: "email"
```

### Creating a new Sign in with Apple identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Sign_in_with_Apple_identity_provider"></a>

The following example creates a Sign in with Apple identity provider in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Sign_in_with_Apple_identity_provider--json"></a>

```
{
  "UserPoolIdentityProvider": {
    "Type": "AWS::Cognito::UserPoolIdentityProvider",
    "Properties": {
      "UserPoolId": {
        "Ref": "UserPool"
      },
      "ProviderName": "SignInWithApple",
      "ProviderDetails": {
        "client_id": "YourAppleServicesId",
        "team_id": "YourAppleTeamId",
        "key_id": "YourApplePrivateKeyID",
        "private_key": "YourApplePrivateKey",
        "authorize_scopes": "public_profile,email"
      },
      "ProviderType": "SignInWithApple",
      "AttributeMapping": {
        "email": "email"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_Sign_in_with_Apple_identity_provider--yaml"></a>

```
UserPoolIdentityProvider:
  Type: AWS::Cognito::UserPoolIdentityProvider
  Properties:
    UserPoolId: !Ref UserPool
    ProviderName: "SignInWithApple"
    ProviderDetails:
      client_id: "YourSign"
      team_id: "YourAppleTeamId",
      key_id: "YourApplePrivateKeyID",
      private_key: "YourApplePrivateKey",
      authorize_scopes: "public_profile,email"
    ProviderType: "Facebook"
    AttributeMapping:
      email: "email"
```

### Creating a new OIDC identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_OIDC_identity_provider"></a>

The following example creates the OIDC identity provider "YourOIDCProviderName" in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_OIDC_identity_provider--json"></a>

```
{
  "UserPoolIdentityProvider": {
    "Type": "AWS::Cognito::UserPoolIdentityProvider",
    "Properties": {
      "UserPoolId": {
        "Ref": "UserPool"
      },
      "ProviderName": "YourOIDCProviderName",
      "ProviderDetails": {
        "client_id": "YourOIDCClientId",
        "client_secret": "YourOIDCClientSecret",
        "attributes_request_method": "GET",
        "oidc_issuer": "YourOIDCIssuerURL",
        "authorize_scopes": "email profile openid"
      },
      "ProviderType": "OIDC",
      "AttributeMapping": {
        "email": "email"
      },
      "IdpIdentifiers": [
        "IdpIdentifier"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_OIDC_identity_provider--yaml"></a>

```
UserPoolIdentityProvider:
  Type: AWS::Cognito::UserPoolIdentityProvider
  Properties:
    UserPoolId: !Ref UserPool
    ProviderName: "YourOIDCProviderName"
    ProviderDetails:
      client_id: "YourOIDCClientId"
      client_secret: "YourOIDCClientSecret"
      attributes_request_method: "GET"
      oidc_issuer: "YourOIDCIssuerURL"
      authorize_scopes: "email profile openid"
    ProviderType: "OIDC"
    AttributeMapping:
      email: "email"
    IdpIdentifiers:
      - "IdpIdentifier"
```

### Creating a new SAML identity provider<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_SAML_identity_provider"></a>

The following example creates a SAML identity provider "YourProviderName" in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_SAML_identity_provider--json"></a>

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
            "email": "Attribute"
         },
         "IdpIdentifiers": [
            "IdpIdentifier"
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-userpoolidentityprovider--examples--Creating_a_new_SAML_identity_provider--yaml"></a>

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
    IdpIdentifiers:
      - "IdpIdentifier"
```