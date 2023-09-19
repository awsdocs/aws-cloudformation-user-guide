# AWS::VerifiedPermissions::IdentitySource<a name="aws-resource-verifiedpermissions-identitysource"></a>

Creates or updates a reference to Amazon Cognito as an external identity provider\. 

If you are creating a new identity source, then you must specify a `Configuration`\. If you are updating an existing identity source, then you must specify an `UpdateConfiguration`\.

After you create an identity source, you can use the identities provided by the IdP as proxies for the principal in authorization queries that use the [IsAuthorizedWithToken](https://docs.aws.amazon.com/verifiedpermissions/latest/apireference/API_IsAuthorizedWithToken.html) operation\. These identities take the form of tokens that contain claims about the user, such as IDs, attributes and group memberships\. Amazon Cognito provides both identity tokens and access tokens, and Verified Permissions can use either or both\. Any combination of identity and access tokens results in the same Cedar principal\. Verified Permissions automatically translates the information about the identities into the standard Cedar attributes that can be evaluated by your policies\. Because the Amazon Cognito identity and access tokens can contain different information, the tokens you choose to use determine the attributes that are available to access in the Cedar principal from your policies\.

Amazon Cognito Identity is not available in all of the same AWS Regions as Amazon Verified Permissions\. Because of this, the `AWS::VerifiedPermissions::IdentitySource` type is not available to create from AWS CloudFormation in Regions where Amazon Cognito Identity is not currently available\. Users can still create `AWS::VerifiedPermissions::IdentitySource` in those Regions, but only from the AWS CLI, Amazon Verified Permissions SDK, or from the AWS console\.

**Note**  
To reference a user from this identity source in your Cedar policies, use the following syntax\.  
*IdentityType::"<CognitoUserPoolIdentifier>\|<CognitoClientId>*  
Where `IdentityType` is the string that you provide to the `PrincipalEntityType` parameter for this operation\. The `CognitoUserPoolId` and `CognitoClientId` are defined by the Amazon Cognito user pool\.

## Syntax<a name="aws-resource-verifiedpermissions-identitysource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-verifiedpermissions-identitysource-syntax.json"></a>

```
{
  "Type" : "AWS::VerifiedPermissions::IdentitySource",
  "Properties" : {
      "[Configuration](#cfn-verifiedpermissions-identitysource-configuration)" : IdentitySourceConfiguration,
      "[PolicyStoreId](#cfn-verifiedpermissions-identitysource-policystoreid)" : String,
      "[PrincipalEntityType](#cfn-verifiedpermissions-identitysource-principalentitytype)" : String
    }
}
```

### YAML<a name="aws-resource-verifiedpermissions-identitysource-syntax.yaml"></a>

```
Type: AWS::VerifiedPermissions::IdentitySource
Properties: 
  [Configuration](#cfn-verifiedpermissions-identitysource-configuration): 
    IdentitySourceConfiguration
  [PolicyStoreId](#cfn-verifiedpermissions-identitysource-policystoreid): String
  [PrincipalEntityType](#cfn-verifiedpermissions-identitysource-principalentitytype): String
```

## Properties<a name="aws-resource-verifiedpermissions-identitysource-properties"></a>

`Configuration`  <a name="cfn-verifiedpermissions-identitysource-configuration"></a>
Contains configuration information used when creating or updating an identity source\.  
At this time, the only valid member of this structure is a Amazon Cognito user pool configuration\.  
You must specify a `userPoolArn`, and optionally, a `ClientId`\.
*Required*: Yes  
*Type*: [IdentitySourceConfiguration](aws-properties-verifiedpermissions-identitysource-identitysourceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyStoreId`  <a name="cfn-verifiedpermissions-identitysource-policystoreid"></a>
Specifies the ID of the policy store in which you want to store this identity source\. Only policies and requests made using this policy store can reference identities from the identity provider configured in the new identity source\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalEntityType`  <a name="cfn-verifiedpermissions-identitysource-principalentitytype"></a>
Specifies the namespace and data type of the principals generated for identities authenticated by the new identity source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-verifiedpermissions-identitysource-return-values"></a>

### Ref<a name="aws-resource-verifiedpermissions-identitysource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the unique id of the new identity source\. For example:

 `{ "Ref": "ISEXAMPLEabcdefg111111" }` 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-verifiedpermissions-identitysource-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-verifiedpermissions-identitysource-return-values-fn--getatt-fn--getatt"></a>

`Details`  <a name="Details-fn::getatt"></a>
A structure that contains information about the configuration of the identity source\.

`Details.ClientIds`  <a name="Details.ClientIds-fn::getatt"></a>
The application client IDs associated with the specified Amazon Cognito user pool that are enabled for this identity source\.

`Details.DiscoveryUrl`  <a name="Details.DiscoveryUrl-fn::getatt"></a>
The well\-known URL that points to this user pool's OIDC discovery endpoint\. This is a URL string in the following format\. This URL replaces the placeholders for both the AWS Region and the user pool identifier with those appropriate for this user pool\.  
`https://cognito-idp.<region>.amazonaws.com/<user-pool-id>/.well-known/openid-configuration`

`Details.OpenIdIssuer`  <a name="Details.OpenIdIssuer-fn::getatt"></a>
A string that identifies the type of OIDC service represented by this identity source\. At this time, the only valid value is `cognito`\.

`Details.UserPoolArn`  <a name="Details.UserPoolArn-fn::getatt"></a>
The [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the Amazon Cognito user pool whose identities are accessible to this Verified Permissions policy store\.

`IdentitySourceId`  <a name="IdentitySourceId-fn::getatt"></a>
The unique ID of the new or updated identity store\.

## Examples<a name="aws-resource-verifiedpermissions-identitysource--examples"></a>



### Creating an identity source for a Amazon Cognito user pool<a name="aws-resource-verifiedpermissions-identitysource--examples--Creating_an_identity_source_for_a__user_pool"></a>

The following example creates an identity source in the specified policy store that points to a Amazon Cognito user pool using the specified client ID\. The new identity source returns objects of the specified data type\.

#### JSON<a name="aws-resource-verifiedpermissions-identitysource--examples--Creating_an_identity_source_for_a__user_pool--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation sample template for creating an identity source for Verified Permissions.",
    "Parameters": {
        "PolicyStoreId": {
            "Type": "String"
        },
        "UserPoolArn": {
            "Type": "String"
        },
        "ClientIds": {
            "Type": "List<String>"
        },
        "PrincipalEntityType": {
            "Type": "String"
        }
    },
    "Resources": {
        "IdentitySource": {
            "Type": "AWS::VerifiedPermissions::IdentitySource",
            "Properties": {
                "PolicyStoreId": {
                    "Ref": "PolicyStoreId"
                },
                "Configuration": {
                    "CognitoUserPoolConfiguration": {
                        "UserPoolArn": {
                            "Ref": "UserPoolArn"
                        },
                        "ClientIds": {
                            "Ref": "ClientIds"
                        }
                    }
                },
                "PrincipalEntityType": {
                    "Ref": "PrincipalEntityType"
                }
            }
        }
    },
    "Outputs": {
        "IdentitySourceId": {
            "Value": {
                "Fn::GetAtt": [
                    "IdentitySource",
                    "IdentitySourceId"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-verifiedpermissions-identitysource--examples--Creating_an_identity_source_for_a__user_pool--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  Description": "AWS CloudFormation sample template for creating an identity source for Verified Permissions
Parameters:
  PolicyStoreId:
    Type: String
  UserPoolArn:
    Type: String
  ClientIds:
    Type: List<String>
  PrincipalEntityType:
    Type: String
Resources:
  IdentitySource:
    Type: AWS::VerifiedPermissions::IdentitySource
    Properties:
      PolicyStoreId: !Ref PolicyStoreId
      Configuration:
        CognitoUserPoolConfiguration:
          UserPoolArn: !Ref UserPoolArn
          ClientIds: !Ref ClientIds
      PrincipalEntityType: !Ref PrincipalEntityType
Outputs:
  IdentitySourceId:
    Value: !GetAtt IdentitySource.IdentitySourceId
```