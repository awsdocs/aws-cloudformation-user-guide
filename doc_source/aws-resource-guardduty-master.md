# AWS::GuardDuty::Master<a name="aws-resource-guardduty-master"></a>

You can use the `AWS::GuardDuty::Master` resource in a GuardDuty member account to accept an invitation to be managed by a GuardDuty master account\. The GuardDuty master account must have already invited the current account \(by calling the InviteMembers API operation or by creating an `AWS::GuardDuty::Member` resource\) before the current account can use the `AWS::GuardDuty::Master` resource to accept the master account's invitation\.

**Topics**
+ [Syntax](#aws-resource-guardduty-master-syntax)
+ [Properties](#aws-resource-guardduty-master-properties)
+ [Return Values](#aws-resource-guardduty-master-returnvalues)
+ [Examples](#aws-resource-guardduty-master-examples)

## Syntax<a name="aws-resource-guardduty-master-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-master-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Master",
  "Properties" : {
    "[DetectorId](#cfn-guardduty-master-detectorid)" : String,
    "[MasterId](#cfn-guardduty-master-masterid)" : String,
    "[InvitationId](#cfn-guardduty-master-invitationid)" : String
  }
}
```

### YAML<a name="aws-resource-guardduty-master-syntax.yaml"></a>

```
Type: "AWS::GuardDuty::Master"
Properties:
  [DetectorId](#cfn-guardduty-master-detectorid): String
  [MasterId](#cfn-guardduty-master-masterid): String
  [InvitationId](#cfn-guardduty-master-invitationid): String
```

## Properties<a name="aws-resource-guardduty-master-properties"></a>

`DetectorId`  <a name="cfn-guardduty-master-detectorid"></a>
The detector ID of the AWS account that is accepting an invitation to become a GuardDuty member account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MasterId`  <a name="cfn-guardduty-master-masterid"></a>
The account ID of the master GuardDuty account whose invitation you're accepting\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InvitationId`  <a name="cfn-guardduty-master-invitationid"></a>
The ID of the invitation that is sent to the AWS account by the GuardDuty master account\. There are several ways to retrieve the invitationId:  
+ By calling the ListInvitation API operation with the GuardDuty member account's credentials\. \(You can also run the following CLI command: `aws guardduty list-invitations`\.\) In the returned results, locate the invitation details \(including the invitationID\) from the GuardDuty master account ID that you would like to accept\.
+ The email account associated with the GuardDuty member account should have received an invitation email from the master account when they invited the current account\. This email contains an acceptance link which has the invitationId\.
+ If you access the member account’s Personal Health Dashboard, you can also see the same invitation email from the master account \(with the invitationId included as part of the invitation acceptance link\)\.
+ If the value for InvitationId is not specified, it can be retrieved by calling [ListInvitations](http://docs.aws.amazon.com/guardduty/latest/ug/list-invitations.html) and receiving the invitation from the given master account ID\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-guardduty-master-returnvalues"></a>

### Ref<a name="aws-resource-guardduty-master-ref"></a>

When you pass the logical ID of an `AWS::GuardDuty::Master` resource to the intrinsic `Ref` function, the function returns the unique ID of the GuardDuty master account, such as `012345678901`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-guardduty-master-examples"></a>

### Declaring a GuardDuty Master Resource<a name="aws-resource-guardduty-master-example1"></a>

The following example shows how to declare an `AWS::GuardDuty::Master` resource to create a GuardDuty master account\.

#### JSON<a name="aws-resource-guardduty-master-example1.json"></a>

```
"GDmaster": {
  "Type": "AWS::GuardDuty::Master",
  "Properties": {
    "DetectorId": "a12abc34d567e8fa901bc2d34e56789f0",
    "MasterId": "012345678901",
    "InvitationId": "84b097800250d17d1872b34c4daadcf5"
   }
}
```

#### YAML<a name="aws-resource-guardduty-master-example1.yaml"></a>

```
GDmaster:
  Type: "AWS::GuardDuty::Master"
  Properties:
    DetectorId: "a12abc34d567e8fa901bc2d34e56789f0"
    MasterId: "012345678901"
    InvitationId: "84b097800250d17d1872b34c4daadcf5"
```