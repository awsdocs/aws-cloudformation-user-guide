# AWS::Cognito::UserPoolRiskConfigurationAttachment<a name="aws-resource-cognito-userpoolriskconfigurationattachment"></a>

The `AWS::Cognito::UserPoolRiskConfigurationAttachment` resource sets the risk configuration that is used for Amazon Cognito advanced security features\.

You can specify risk configuration for a single client \(with a specific `clientId`\) or for all clients \(by setting the `clientId` to `ALL`\)\. If you specify `ALL`, the default configuration is used for every client that has had no risk configuration set previously\. If you specify risk configuration for a particular client, it no longer falls back to the `ALL` configuration\.

## Syntax<a name="aws-resource-cognito-userpoolriskconfigurationattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolriskconfigurationattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolRiskConfigurationAttachment",
  "Properties" : {
      "[AccountTakeoverRiskConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoverriskconfiguration)" : AccountTakeoverRiskConfigurationType,
      "[ClientId](#cfn-cognito-userpoolriskconfigurationattachment-clientid)" : String,
      "[CompromisedCredentialsRiskConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfiguration)" : CompromisedCredentialsRiskConfigurationType,
      "[RiskExceptionConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfiguration)" : RiskExceptionConfigurationType,
      "[UserPoolId](#cfn-cognito-userpoolriskconfigurationattachment-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolriskconfigurationattachment-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolRiskConfigurationAttachment
Properties: 
  [AccountTakeoverRiskConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoverriskconfiguration): 
    AccountTakeoverRiskConfigurationType
  [ClientId](#cfn-cognito-userpoolriskconfigurationattachment-clientid): String
  [CompromisedCredentialsRiskConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfiguration): 
    CompromisedCredentialsRiskConfigurationType
  [RiskExceptionConfiguration](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfiguration): 
    RiskExceptionConfigurationType
  [UserPoolId](#cfn-cognito-userpoolriskconfigurationattachment-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpoolriskconfigurationattachment-properties"></a>

`AccountTakeoverRiskConfiguration`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoverriskconfiguration"></a>
The account takeover risk configuration object including the `NotifyConfiguration` object and `Actions` to take in the case of an account takeover\.  
*Required*: No  
*Type*: [AccountTakeoverRiskConfigurationType](aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoverriskconfigurationtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientId`  <a name="cfn-cognito-userpoolriskconfigurationattachment-clientid"></a>
The app client ID\. You can specify the risk configuration for a single client \(with a specific ClientId\) or for all clients \(by setting the ClientId to `ALL`\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CompromisedCredentialsRiskConfiguration`  <a name="cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfiguration"></a>
The compromised credentials risk configuration object including the `EventFilter` and the `EventAction`   
*Required*: No  
*Type*: [CompromisedCredentialsRiskConfigurationType](aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RiskExceptionConfiguration`  <a name="cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfiguration"></a>
The configuration to override the risk decision\.  
*Required*: No  
*Type*: [RiskExceptionConfigurationType](aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolriskconfigurationattachment-userpoolid"></a>
The user pool ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpoolriskconfigurationattachment-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolriskconfigurationattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the physicalResourceId, which is “UserPoolRiskConfigurationAttachment\-UserPoolId\-ClientId"\. For example:

 `{ "Ref": “UserPoolRiskConfigurationAttachment-us-east-1_FAKEPOOLID-2asc123fakeclientidajjulj6bh” }` 

For the Amazon Cognito risk configuration attachment `UserPoolRiskConfigurationAttachment-us-east-1_FAKEPOOLID-2asc123fakeclientidajjulj6bh`, Ref returns the name of the risk configuration attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpoolriskconfigurationattachment--examples"></a>



### Creating a new risk configuration attachment for a user pool<a name="aws-resource-cognito-userpoolriskconfigurationattachment--examples--Creating_a_new_risk_configuration_attachment_for_a_user_pool"></a>

The following example sets risk configurations in the referenced user pool and client\.

#### JSON<a name="aws-resource-cognito-userpoolriskconfigurationattachment--examples--Creating_a_new_risk_configuration_attachment_for_a_user_pool--json"></a>

```
{
   "UserPoolRiskConfiguration":{
      "Type":"AWS::Cognito::UserPoolRiskConfigurationAttachment",
      "Properties":{
         "UserPoolId":{
            "Ref":"UserPool"
         },
         "ClientId":{
            "Ref":"Client"
         },
         "AccountTakeoverRiskConfiguration":{
            "Actions":{
               "HighAction":{
                  "EventAction":"MFA_REQUIRED",
                  "Notify":true,

               },
               "MediumAction":{
                  "EventAction":"MFA_IF_CONFIGURED",
                  "Notify":true
               },
               "LowAction":{
                  "EventAction":{
                     "Ref":"EventAction"
                  },
                  "Notify":false
               }
            },
            "NotifyConfiguration":{
               "BlockEmail":{
                  "HtmlBody":"html body",
                  "Subject":"Your account got blocked",
                  "TextBody":"Your account got blocked"
               },
               "MfaEmail":{
                  "HtmlBody":"html body",
                  "Subject":"Your account needs MFA verification",
                  "TextBody":"Your account needs MFA verification"
               },
               "NoActionEmail":{
                  "HtmlBody":{
                     "Ref":"HtmlBody"
                  },
                  "Subject":{
                     "Ref":"Subject"
                  },
                  "TextBody":{
                     "Ref":"TextBody"
                  },

               },
               "From":"your-from-email@amazon.com",
               "SourceArn":{
                  "Ref":"SourceArn"
               },
               "ReplyTo":"your-reply-to@amazon.com"
            }
         },
         "CompromisedCredentialsRiskConfiguration":{
            "Actions":{
               "EventAction":"BLOCKED"
            },
            "EventFilter":[
               {
                  "Ref":"EventFilter"
               },

            ]
         },
         "RiskExceptionConfiguration":{
            "BlockedIPRangeList":[
               "198.0.0.1"
            ],
            "SkippedIPRangeList":[
               "198.0.0.1"
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-userpoolriskconfigurationattachment--examples--Creating_a_new_risk_configuration_attachment_for_a_user_pool--yaml"></a>

```
UserPoolRiskConfiguration: 
  Type: AWS::Cognito::UserPoolRiskConfigurationAttachment 
  Properties: 
    UserPoolId: !Ref UserPool
    ClientId: !Ref Client 
    AccountTakeoverRiskConfiguration: 
      Actions: 
        HighAction: 
          EventAction: "MFA_REQUIRED" 
          Notify: True 
        MediumAction: 
          EventAction: "MFA_IF_CONFIGURED" 
          Notify: True
        LowAction: 
          EventAction: !Ref LowEventAction 
          Notify: False 
      NotifyConfiguration: 
        BlockEmail:
          HtmlBody: "html body" 
          Subject: "Your account got blocked" 
          TextBody: "Your account got blocked" 
        MfaEmail: 
          HtmlBody: "html body" 
          Subject: "Your account needs MFA verification"
          TextBody: "Your account needs MFA verification" 
        NoActionEmail: 
          HtmlBody: !Ref HtmlBody
          Subject: !Ref Subject 
          TextBody: !Ref TextBody 
        From: "your-from-email@amazon.com" 
        SourceArn: !Ref SourceArn 
        ReplyTo: "your-reply-to@amazon.com" 
    CompromisedCredentialsRiskConfiguration:
      Actions: 
        EventAction: "BLOCKED" 
        EventFilter: - !Ref EventFilter 
    RiskExceptionConfiguration:
        BlockedIPRangeList: 
          - "198.0.0.1" 
        SkippedIPRangeList: 
          - "198.0.0.1"
```