# AWS::Cognito::IdentityPoolRoleAttachment<a name="aws-resource-cognito-identitypoolroleattachment"></a>

The `AWS::Cognito::IdentityPoolRoleAttachment` resource manages the role configuration for an Amazon Cognito identity pool\.

## Syntax<a name="aws-resource-cognito-identitypoolroleattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-identitypoolroleattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::IdentityPoolRoleAttachment",
  "Properties" : {
      "[IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid)" : String,
      "[RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings)" : Json,
      "[Roles](#cfn-cognito-identitypoolroleattachment-roles)" : Json
    }
}
```

### YAML<a name="aws-resource-cognito-identitypoolroleattachment-syntax.yaml"></a>

```
Type: AWS::Cognito::IdentityPoolRoleAttachment
Properties: 
  [IdentityPoolId](#cfn-cognito-identitypoolroleattachment-identitypoolid): String
  [RoleMappings](#cfn-cognito-identitypoolroleattachment-rolemappings): Json
  [Roles](#cfn-cognito-identitypoolroleattachment-roles): Json
```

## Properties<a name="aws-resource-cognito-identitypoolroleattachment-properties"></a>

`IdentityPoolId`  <a name="cfn-cognito-identitypoolroleattachment-identitypoolid"></a>
An identity pool ID in the format `REGION:GUID`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleMappings`  <a name="cfn-cognito-identitypoolroleattachment-rolemappings"></a>
How users for a specific identity provider are mapped to roles\. This is a string to the `RoleMapping` object map\. The string identifies the identity provider\. For example: "graph\.facebook\.com" or "cognito\-idp\.us\-east\-1\.amazonaws\.com/us\-east\-1\_abcdefghi:app\_client\_id"\.  
If the `IdentityProvider` field isn't provided in this object, the string is used as the identity provider name\.  
For more information, see the [RoleMapping property](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-identitypoolroleattachment-rolemapping.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Roles`  <a name="cfn-cognito-identitypoolroleattachment-roles"></a>
The map of the roles associated with this pool\. For a given role, the key is either "authenticated" or "unauthenticated"\. The value is the role ARN\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cognito-identitypoolroleattachment-return-values"></a>

### Ref<a name="aws-resource-cognito-identitypoolroleattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a generated ID, such as `IdentityPoolRoleAttachment-EXAMPLEwnOR3n`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-identitypoolroleattachment--examples"></a>



### Setting the roles for an identity pool<a name="aws-resource-cognito-identitypoolroleattachment--examples--Setting_the_roles_for_an_identity_pool"></a>

The following example sets roles for an identity pool\. It sets “authenticated” and “unauthenticated” roles and maps two identity providers to them\. The first identity provider is “graph\.facebook\.com”\. The second is using a reference to set the identity provider name\.

#### JSON<a name="aws-resource-cognito-identitypoolroleattachment--examples--Setting_the_roles_for_an_identity_pool--json"></a>

```
{
   "IdentityPoolRoleAttachment":{
      "Type":"AWS::Cognito::IdentityPoolRoleAttachment",
      "Properties":{
         "IdentityPoolId":{
            "Ref":"IdentityPool"
         },
         "Roles":{
            "authenticated":{
               "Fn::GetAtt":[
                  "AuthenticatedRole",
                  "Arn"
               ]
            },
            "unauthenticated":{
               "Fn::GetAtt":[
                  "UnAuthenticatedRole",
                  "Arn"
               ]
            }
         },
         "RoleMappings":{
            "graph.facebook.com":{
               "IdentityProvider":"graph.facebook.com",
               "AmbiguousRoleResolution":"Deny",
               "Type":"Rules",
               "RulesConfiguration":{
                  "Rules":[
                     {
                        "Claim":"sub",
                        "MatchType":"Equals",
                        "RoleARN":{
                           "Fn::GetAtt":[
                              "AuthenticatedRole",
                              "Arn"
                           ]
                        },
                        "Value":"goodvalue"
                     }
                  ]
               }
            },
            "userpool1":{
               "IdentityProvider":{
                  "Ref":"CognitoUserPool"
               },
               "AmbiguousRoleResolution":"Deny",
               "Type":"Rules",
               "RulesConfiguration":{
                  "Rules":[
                     {
                        "Claim":"sub",
                        "MatchType":"Equals",
                        "RoleARN":{
                           "Fn::GetAtt":[
                              "AuthenticatedRole",
                              "Arn"
                           ]
                        },
                        "Value":"goodvalue"
                     }
                  ]
               }
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-identitypoolroleattachment--examples--Setting_the_roles_for_an_identity_pool--yaml"></a>

```
IdentityPoolRoleAttachment: 
  Type: AWS::Cognito::IdentityPoolRoleAttachment 
  Properties: 
    IdentityPoolId: !Ref IdentityPool
    Roles: 
      "authenticated": !GetAtt AuthenticatedRole.Arn 
      "unauthenticated": !GetAtt UnAuthenticatedRole.Arn 
    RoleMappings:  
      "graph.facebook.com":
        IdentityProvider: "graph.facebook.com" 
        AmbiguousRoleResolution: Deny 
        Type: Rules 
        RulesConfiguration: 
          Rules: 
            - Claim: "sub" 
              MatchType: "Equals" 
              RoleARN: !GetAtt AuthenticatedRole.Arn 
              Value: "goodvalue"
      "userpool1": 
        IdentityProvider: !Ref CognitoUserPool 
        AmbiguousRoleResolution: Deny 
        Type: Rules 
        RulesConfiguration: 
          Rules: 
            - Claim: "sub" 
              MatchType: "Equals" 
              RoleARN: !GetAtt AuthenticatedRole.Arn 
              Value: "goodvalue"
```