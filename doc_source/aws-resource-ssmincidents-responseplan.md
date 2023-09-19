# AWS::SSMIncidents::ResponsePlan<a name="aws-resource-ssmincidents-responseplan"></a>

The `AWS::SSMIncidents::ResponsePlan` resource specifies the details of the response plan that are used when creating an incident\.

## Syntax<a name="aws-resource-ssmincidents-responseplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmincidents-responseplan-syntax.json"></a>

```
{
  "Type" : "AWS::SSMIncidents::ResponsePlan",
  "Properties" : {
      "[Actions](#cfn-ssmincidents-responseplan-actions)" : [ Action, ... ],
      "[ChatChannel](#cfn-ssmincidents-responseplan-chatchannel)" : ChatChannel,
      "[DisplayName](#cfn-ssmincidents-responseplan-displayname)" : String,
      "[Engagements](#cfn-ssmincidents-responseplan-engagements)" : [ String, ... ],
      "[IncidentTemplate](#cfn-ssmincidents-responseplan-incidenttemplate)" : IncidentTemplate,
      "[Integrations](#cfn-ssmincidents-responseplan-integrations)" : [ Integration, ... ],
      "[Name](#cfn-ssmincidents-responseplan-name)" : String,
      "[Tags](#cfn-ssmincidents-responseplan-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssmincidents-responseplan-syntax.yaml"></a>

```
Type: AWS::SSMIncidents::ResponsePlan
Properties: 
  [Actions](#cfn-ssmincidents-responseplan-actions): 
    - Action
  [ChatChannel](#cfn-ssmincidents-responseplan-chatchannel): 
    ChatChannel
  [DisplayName](#cfn-ssmincidents-responseplan-displayname): String
  [Engagements](#cfn-ssmincidents-responseplan-engagements): 
    - String
  [IncidentTemplate](#cfn-ssmincidents-responseplan-incidenttemplate): 
    IncidentTemplate
  [Integrations](#cfn-ssmincidents-responseplan-integrations): 
    - Integration
  [Name](#cfn-ssmincidents-responseplan-name): String
  [Tags](#cfn-ssmincidents-responseplan-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssmincidents-responseplan-properties"></a>

`Actions`  <a name="cfn-ssmincidents-responseplan-actions"></a>
The actions that the response plan starts at the beginning of an incident\.  
*Required*: No  
*Type*: List of [Action](aws-properties-ssmincidents-responseplan-action.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChatChannel`  <a name="cfn-ssmincidents-responseplan-chatchannel"></a>
The AWS Chatbot chat channel used for collaboration during an incident\.  
*Required*: No  
*Type*: [ChatChannel](aws-properties-ssmincidents-responseplan-chatchannel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-ssmincidents-responseplan-displayname"></a>
The human readable name of the response plan\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engagements`  <a name="cfn-ssmincidents-responseplan-engagements"></a>
The Amazon Resource Name \(ARN\) for the contacts and escalation plans that the response plan engages during an incident\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncidentTemplate`  <a name="cfn-ssmincidents-responseplan-incidenttemplate"></a>
Details used to create an incident when using this response plan\.  
*Required*: Yes  
*Type*: [IncidentTemplate](aws-properties-ssmincidents-responseplan-incidenttemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Integrations`  <a name="cfn-ssmincidents-responseplan-integrations"></a>
Information about third\-party services integrated into the response plan\.  
*Required*: No  
*Type*: List of [Integration](aws-properties-ssmincidents-responseplan-integration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssmincidents-responseplan-name"></a>
The name of the response plan\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ssmincidents-responseplan-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-ssmincidents-responseplan--examples"></a>

### Create a response plan<a name="aws-resource-ssmincidents-responseplan--examples--Create_a_response_plan"></a>

The following example creates a response plan\.

**Note**  
This example also demonstrates creating a replication set\. We recommend creating a replication set and response plan using a single template\. This template also incorporates resources from [AWS Systems Manager Incident Manager Contacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_SSMContacts.html)\.

#### JSON<a name="aws-resource-ssmincidents-responseplan--examples--Create_a_response_plan--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Sample AWS CloudFormation template to create a response plan and replication set (JSON).",
   "Parameters": {
      "ContactEmail": {
         "Type": "String",
         "Description": "The email address to use to engage the contact channel."
      },
      "ChatbotSnsArn": {
         "Type": "String",
         "Description": "The Amazon Simple Notification Service (SNS) targets that AWS Chatbot uses to provide the chat channel with updates about an incident."
      },
      "NotificationTargetArn": {
         "Type": "String",
         "Description": "The SNS topic used by AWS Chatbot to send notifications to the incidents chat channel.",
         "AllowedPattern": "^arn:aws(-cn|-us-gov)?:[a-z0-9-]*:[a-z0-9-]*:([0-9]{12})?:.+$"
      },
      "SsmRoleArn": {
         "Type": "String",
         "Description": "The Amazon Resource Name (ARN) of the role that the Automation runbook assumes when running commands.",
         "AllowedPattern": "^arn:aws(-cn|-us-gov)?:iam::([0-9]{12})?:role/.+$"
      },
      "SsmAutomationDocument": {
         "Type": "String",
         "Description": "The Systems Manager Automation runbook to use during an incident.",
         "AllowedPattern": "^[a-zA-Z0-9_\\-.:/]{3,128}$"
      }
   },
   "Resources": {
      "MyReplicationSet": {
         "Type": "AWS::SSMIncidents::ReplicationSet",
         "Properties": {
            "Regions": [
               {
                  "RegionName": {
                     "Ref": "AWS::Region"
                  }
               }
            ],
            "Tags": [
               {
                  "Key": "MyReplicationSetTagKey",
                  "Value": "MyReplicationSetTagValue"
               }
            ]
         }
      },
      "MyIncidentsResponsePlan": {
         "Type": "AWS::SSMIncidents::ResponsePlan",
         "Properties": {
            "Name": "MyResponsePlan",
            "ChatChannel": {
               "ChatbotSns": "ChatbotSnsArn"
            },
            "Engagements": "MyEscalationPlanContact",
            "Actions": [
               {
                  "SsmAutomation": {
                     "RoleArn": "SsmRoleArn",
                     "DocumentName": "SsmAutomationDocument",
                     "DocumentVersion": "1",
                     "TargetAccount": "IMPACTED_ACCOUNT",
                     "Parameters": [
                        {
                           "Key": "Key1",
                           "Values": [
                              "Value1"
                           ]
                        }
                     ],
                     "DynamicParameters": [
                        {
                           "Key": "Key2",
                           "Value": {
                              "Variable": "INCIDENT_RECORD_ARN"
                           }
                        },
                        {
                           "Key": "Key3",
                           "Value": {
                              "Variable": "INVOLVED_RESOURCES"
                           }
                        }
                     ]
                  }
               }
            ],
            "IncidentTemplate": {
               "Title": "MyIncident",
               "Impact": 1,
               "Summary": "My incident summary.",
               "DedupeString": "MyDedupeString",
               "NotificationTargets": [
                  {
                     "SnsTopicArn": "NotificationTargetArn"
                  }
               ],
               "IncidentTags": [
                  {
                     "Key": "MyIncidentTagKey",
                     "Value": "MyIncidentTagValue"
                  }
               ]
            },
            "Tags": [
               {
                  "Key": "MyResponsePlanTagKey",
                  "Value": "MyResponsePlanTagValue"
               }
            ]
         },
         "DependsOn": "MyReplicationSet"
      },
      "MyContactChannelEmail": {
         "Type": "AWS::SSMContacts::ContactChannel",
         "Properties": {
            "ContactId": "MySSMContact",
            "ChannelName": "emailChannel",
            "ChannelType": "EMAIL",
            "ChannelAddress": "ContactEmail"
         },
         "DependsOn": "MyReplicationSet"
      },
      "MySSMContact": {
         "Type": "AWS::SSMContacts::Contact",
         "Properties": {
            "Alias": "my-ssm-contact",
            "DisplayName": "MySSMContact",
            "Type": "PERSONAL"
         },
         "DependsOn": "MyReplicationSet"
      },
      "MySSMContactEngagementPlan": {
         "Type": "AWS::SSMContacts::Plan",
         "Properties": {
            "ContactId": "MySSMContact",
            "Stages": [
               {
                  "DurationInMinutes": 10,
                  "Targets": [
                     {
                        "ChannelTargetInfo": {
                           "ChannelId": "MyContactChannelEmail",
                           "RetryIntervalInMinutes": 3
                        }
                     }
                  ]
               }
            ]
         },
         "DependsOn": "MyReplicationSet"
      },
      "MyEscalationPlanContact": {
         "Type": "AWS::SSMContacts::Contact",
         "Properties": {
            "Alias": "my-escalation-plan",
            "DisplayName": "MyEscalationPlan",
            "Type": "ESCALATION"
         },
         "DependsOn": "MyReplicationSet"
      },
      "MyEscalationPlan": {
         "Type": "AWS::SSMContacts::Plan",
         "Properties": {
            "ContactId": "MyEscalationPlanContact",
            "Stages": [
               {
                  "DurationInMinutes": 0,
                  "Targets": [
                     {
                        "ContactTargetInfo": {
                           "ContactId": "MySSMContact",
                           "IsEssential": true
                        }
                     }
                  ]
               }
            ]
         },
         "DependsOn": "MyReplicationSet"
      }
   },
   "Outputs": {
      "ReplicationSetArn": {
         "Value": "MyReplicationSet"
      },
      "Region": {
         "Value": "AWS::Region"
      },
      "SSMContactArn": {
         "Value": "MySSMContact"
      },
      "EscalationPlanArn": {
         "Value": "MyEscalationPlanContact"
      },
      "ResponsePlanArn": {
         "Value": "MyIncidentsResponsePlan"
      }
   }
}
```

#### YAML<a name="aws-resource-ssmincidents-responseplan--examples--Create_a_response_plan--yaml"></a>

```
---
AWSTemplateFormatVersion: 2010-09-09
Description: "Sample AWS CloudFormation template to create a response plan and replication set (YAML)."
Parameters:
  ContactEmail:
    Type: String
    Description: The email address to use to engage the contact channel.
  ChatbotSnsArn:
    Type: String
    Description: The Amazon Simple Notification Service (SNS) targets that AWS
      Chatbot uses to provide the chat channel with updates about an incident.
  NotificationTargetArn:
    Type: String
    Description: The SNS topic used by AWS Chatbot to send notifications to the
      incidents chat channel.
    AllowedPattern: ^arn:aws(-cn|-us-gov)?:[a-z0-9-]*:[a-z0-9-]*:([0-9]{12})?:.+$
  SsmRoleArn:
    Type: String
    Description: The Amazon Resource Name (ARN) of the role that the Automation
      runbook assumes when running commands.
    AllowedPattern: ^arn:aws(-cn|-us-gov)?:iam::([0-9]{12})?:role/.+$
  SsmAutomationDocument:
    Type: String
    Description: The Systems Manager Automation runbook to use during an incident.
    AllowedPattern: ^[a-zA-Z0-9_\-.:/]{3,128}$
Resources:
  MyReplicationSet:
    Type: AWS::SSMIncidents::ReplicationSet
    Properties:
      Regions:
        - RegionName:
            Ref: AWS::Region
      Tags:
        - Key: MyReplicationSetTagKey
          Value: MyReplicationSetTagValue
  MyIncidentsResponsePlan:
    Type: AWS::SSMIncidents::ResponsePlan
    Properties:
      Name: MyResponsePlan
      ChatChannel:
        ChatbotSns: ChatbotSnsArn
      Engagements: MyEscalationPlanContact
      Actions:
        - SsmAutomation:
            RoleArn: SsmRoleArn
            DocumentName: SsmAutomationDocument
            DocumentVersion: "1"
            TargetAccount: IMPACTED_ACCOUNT
            Parameters:
              - Key: Key1
                Values:
                  - Value1
            DynamicParameters:
              - Key: Key2
                Value:
                  Variable: INCIDENT_RECORD_ARN
              - Key: Key3
                Value:
                  Variable: INVOLVED_RESOURCES
      IncidentTemplate:
        Title: MyIncident
        Impact: 1
        Summary: "My incident summary."
        DedupeString: MyDedupeString
        NotificationTargets:
          - SnsTopicArn: NotificationTargetArn
        IncidentTags:
          - Key: MyIncidentTagKey
            Value: MyIncidentTagValue
      Tags:
        - Key: MyResponsePlanTagKey
          Value: MyResponsePlanTagValue
    DependsOn: MyReplicationSet
  MyContactChannelEmail:
    Type: AWS::SSMContacts::ContactChannel
    Properties:
      ContactId: MySSMContact
      ChannelName: emailChannel
      ChannelType: EMAIL
      ChannelAddress: ContactEmail
    DependsOn: MyReplicationSet
  MySSMContact:
    Type: AWS::SSMContacts::Contact
    Properties:
      Alias: my-ssm-contact
      DisplayName: MySSMContact
      Type: PERSONAL
    DependsOn: MyReplicationSet
  MySSMContactEngagementPlan:
    Type: AWS::SSMContacts::Plan
    Properties:
      ContactId: MySSMContact
      Stages:
        - DurationInMinutes: 10
          Targets:
            - ChannelTargetInfo:
                ChannelId: MyContactChannelEmail
                RetryIntervalInMinutes: 3
    DependsOn: MyReplicationSet
  MyEscalationPlanContact:
    Type: AWS::SSMContacts::Contact
    Properties:
      Alias: my-escalation-plan
      DisplayName: MyEscalationPlan
      Type: ESCALATION
    DependsOn: MyReplicationSet
  MyEscalationPlan:
    Type: AWS::SSMContacts::Plan
    Properties:
      ContactId: MyEscalationPlanContact
      Stages:
        - DurationInMinutes: 0
          Targets:
            - ContactTargetInfo:
                ContactId: MySSMContact
                IsEssential: true
    DependsOn: MyReplicationSet
Outputs:
  ReplicationSetArn:
    Value: MyReplicationSet
  Region:
    Value: AWS::Region
  SSMContactArn:
    Value: MySSMContact
  EscalationPlanArn:
    Value: MyEscalationPlanContact
  ResponsePlanArn:
    Value: MyIncidentsResponsePlan
```