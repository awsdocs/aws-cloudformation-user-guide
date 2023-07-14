# AWS::Shield::ProactiveEngagement<a name="aws-resource-shield-proactiveengagement"></a>

Authorizes the Shield Response Team \(SRT\) to use email and phone to notify contacts about escalations to the SRT and to initiate proactive customer support\.

To enable proactive engagement, you must be subscribed to the [Business Support plan](http://aws.amazon.com/premiumsupport/business-support/) or the [Enterprise Support plan](http://aws.amazon.com/premiumsupport/enterprise-support/)\. 

**Note**  
To configure this resource through AWS CloudFormation, you must be subscribed to AWS Shield Advanced\. You can subscribe through the [Shield Advanced console](https://console.aws.amazon.com/wafv2/shieldv2#/) and through the APIs\. For more information, see [Subscribe to AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/enable-ddos-prem.html)\. 

See example templates for Shield Advanced in AWS CloudFormation at [aws\-samples/aws\-shield\-advanced\-examples](https://github.com/aws-samples/aws-shield-advanced-examples)\. 

## Syntax<a name="aws-resource-shield-proactiveengagement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-shield-proactiveengagement-syntax.json"></a>

```
{
  "Type" : "AWS::Shield::ProactiveEngagement",
  "Properties" : {
      "[EmergencyContactList](#cfn-shield-proactiveengagement-emergencycontactlist)" : [ EmergencyContact, ... ],
      "[ProactiveEngagementStatus](#cfn-shield-proactiveengagement-proactiveengagementstatus)" : String
    }
}
```

### YAML<a name="aws-resource-shield-proactiveengagement-syntax.yaml"></a>

```
Type: AWS::Shield::ProactiveEngagement
Properties: 
  [EmergencyContactList](#cfn-shield-proactiveengagement-emergencycontactlist): 
    - EmergencyContact
  [ProactiveEngagementStatus](#cfn-shield-proactiveengagement-proactiveengagementstatus): String
```

## Properties<a name="aws-resource-shield-proactiveengagement-properties"></a>

`EmergencyContactList`  <a name="cfn-shield-proactiveengagement-emergencycontactlist"></a>
The list of email addresses and phone numbers that the Shield Response Team \(SRT\) can use to contact you for escalations to the SRT and to initiate proactive customer support, plus any relevant notes\.   
To enable proactive engagement, the contact list must include at least one phone number\.  
If you provide more than one contact, in the notes, indicate the circumstances under which each contact should be used\. Include primary and secondary contact designations, and provide the hours of availability and time zones for each contact\.  
Example contact notes:  
+ This is a hotline that's staffed 24x7x365\. Please work with the responding analyst and they will get the appropriate person on the call\.
+ Please contact the secondary phone number if the hotline doesn't respond within 5 minutes\.
*Required*: Yes  
*Type*: List of [EmergencyContact](aws-properties-shield-proactiveengagement-emergencycontact.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProactiveEngagementStatus`  <a name="cfn-shield-proactiveengagement-proactiveengagementstatus"></a>
Specifies whether proactive engagement is enabled or disabled\.   
Valid values:   
`ENABLED` \- The Shield Response Team \(SRT\) will use email and phone to notify contacts about escalations to the SRT and to initiate proactive customer support\.  
`DISABLED` \- The SRT will not proactively notify contacts about escalations or to initiate proactive customer support\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-shield-proactiveengagement-return-values"></a>

### Ref<a name="aws-resource-shield-proactiveengagement-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the account that submitted the template\. 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-shield-proactiveengagement-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-shield-proactiveengagement-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
The ID of the account that submitted the template\.

## Examples<a name="aws-resource-shield-proactiveengagement--examples"></a>



### Enable proactive engagement and define contacts<a name="aws-resource-shield-proactiveengagement--examples--Enable_proactive_engagement_and_define_contacts"></a>

The following shows an example proactive engagement configuration with proactive engagement enabled and with two emergency contacts\. 

#### YAML<a name="aws-resource-shield-proactiveengagement--examples--Enable_proactive_engagement_and_define_contacts--yaml"></a>

```
Resources:
  TestProactiveEngagement:
    DeletionPolicy: Delete
    Type: AWS::Shield::ProactiveEngagement
    Properties:
      ProactiveEngagementStatus: ENABLED
      EmergencyContactList:
        - EmailAddress: !Sub 'dev-on-duty@example.com'
          ContactNotes: !Sub 'Dev On Duty'
          PhoneNumber: '+10000000001'
        - EmailAddress: !Sub 'security@example.com'
          ContactNotes: !Sub 'Security Team'
          PhoneNumber: '+10000000002'
```

#### JSON<a name="aws-resource-shield-proactiveengagement--examples--Enable_proactive_engagement_and_define_contacts--json"></a>

```
{
    "Resources": {
        "TestProactiveEngagement": {
            "DeletionPolicy": "Delete",
            "Type": "AWS::Shield::ProactiveEngagement",
            "Properties": {
                "ProactiveEngagementStatus": "ENABLED",
                "EmergencyContactList": [
                    {
                        "EmailAddress": {
                            "Fn::Sub": "dev-on-duty@example.com"
                        },
                        "ContactNotes": {
                            "Fn::Sub": "Dev On Duty"
                        },
                        "PhoneNumber": "+10000000001"
                    },
                    {
                        "EmailAddress": {
                            "Fn::Sub": "security@example.com"
                        },
                        "ContactNotes": {
                            "Fn::Sub": "Security Team"
                        },
                        "PhoneNumber": "+10000000002"
                    }
                ]
            }
        }
    }
}
```