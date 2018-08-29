# AWS::GuardDuty::Member<a name="aws-resource-guardduty-member"></a>

You can use the `AWS::GuardDuty::Member` resource to add an AWS account as a GuardDuty member account to the current GuardDuty master account\. If the value of the Status property is not provided or set to CREATED, a member account is only created\. If the value of the Status property is set to INVITED, a member account is created and invited\. `AWS::GuardDuty::Member` resource has to be created with the Status property set to INVITED before the `AWS::GuardDuty::Master` resource can be created in a GuardDuty member account\.

**Topics**
+ [Syntax](#aws-resource-guardduty-member-syntax)
+ [Properties](#aws-resource-guardduty-member-properties)
+ [Return Values](#aws-resource-guardduty-member-returnvalues)
+ [Examples](#aws-resource-guardduty-member-examples)

## Syntax<a name="aws-resource-guardduty-member-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-member-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Member",
  "Properties" : {
    "[Status](#cfn-guardduty-member-status)" : String,
    "[MemberId](#cfn-guardduty-member-memberid)" : String,
    "[Email](#cfn-guardduty-member-email)" : String,
    "[Message](#cfn-guardduty-member-message)" : String,
    "[DetectorId](#cfn-guardduty-member-detectorid)" : String,
    "[DisableEmailNotification](#cfn-guardduty-member-disableemailnotification)" : Boolean 
  }
}
```

### YAML<a name="aws-resource-guardduty-member-syntax.yaml"></a>

```
Type: "AWS::GuardDuty::Member"
Properties:
  [Status](#cfn-guardduty-member-status): String
  [MemberId](#cfn-guardduty-member-memberid): String
  [Email](#cfn-guardduty-member-email): String
  [Message](#cfn-guardduty-member-message): String
  [DetectorId](#cfn-guardduty-member-detectorid): String
  [DisableEmailNotification](#cfn-guardduty-member-disableemailnotification): Boolean
```

## Properties<a name="aws-resource-guardduty-member-properties"></a>

`Status`  <a name="cfn-guardduty-member-status"></a>
You can use this property to update the status of the relationship between the member account and its master account\. Valid values are CREATED \| INVITED \| DISABLED \| ENABLED \| REMOVED \| RESIGNED\. If the value for this property is not provided or set to CREATED, a member account is only created\. If the value of this property is set to INVITED, a member account is created and invited\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MemberId`  <a name="cfn-guardduty-member-memberid"></a>
The account ID of the member GuardDuty account\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Email`  <a name="cfn-guardduty-member-email"></a>
The email address of the GuardDuty member account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Message`  <a name="cfn-guardduty-member-message"></a>
The invitation message that you want to send to the account that you invite to GuardDuty as a member\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DetectorId`  <a name="cfn-guardduty-member-detectorid"></a>
The unique ID of the detector in a GuardDuty master account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DisableEmailNotification`  <a name="cfn-guardduty-member-disableemailnotification"></a>
Specifies whether an email notification is sent to the accounts that you want to invite to GuardDuty as members\. When set to 'True', email notification is not sent to the invitees\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-guardduty-member-returnvalues"></a>

### Ref<a name="aws-resource-guardduty-member-ref"></a>

When you pass the logical ID of an `AWS::GuardDuty::Member` resource to the intrinsic `Ref` function, the function returns the unique ID of the GuardDuty member account, such as `012345678901`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-guardduty-member-examples"></a>

### Declaring a GuardDuty Member Resource<a name="aws-resource-guardduty-member-example1"></a>

The following example shows how to declare an AWS::GuardDuty::Member resource to create a GuardDuty member account\.

#### JSON<a name="aws-resource-guardduty-member-example1.json"></a>

```
"GDmaster": {
  "Type": "AWS::GuardDuty::Member",
  "Properties": {
    "Status": "Invited",    
    "MemberId": "012345678901",
    "Email": "guarddutymember@amazon.com",
    "Message": "You are invited to enable Amazon Guardduty.",
    "DetectorId": "a12abc34d567e8fa901bc2d34e56789f0",
    "DisableEmailNotification": true
    }
}
```

#### YAML<a name="aws-resource-guardduty-member-example1.yaml"></a>

```
GDmaster:
  Type: "AWS::GuardDuty::Member"
  Properties:
    Status: "Invited"    
    MemberId: "012345678901"
    Email: "guarddutymember@amazon.com"
    Message: "You are invited to enable Amazon Guardduty."
    DetectorId: "a12abc34d567e8fa901bc2d34e56789f0"
    DisableEmailNotification: true
```