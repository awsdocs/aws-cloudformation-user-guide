# AWS::GuardDuty::Member<a name="aws-resource-guardduty-member"></a>

You can use the `AWS::GuardDuty::Member` resource to add an AWS account as a GuardDuty member account to the current GuardDuty master account\. If the value of the `Status` property is not provided or is set to `Created`, a member account is created but not invited\. If the value of the `Status` property is set to `Invited`, a member account is created and invited\. An `AWS::GuardDuty::Member` resource must be created with the `Status` property set to `Invited` before the `AWS::GuardDuty::Master` resource can be created in a GuardDuty member account\.

## Syntax<a name="aws-resource-guardduty-member-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-member-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Member",
  "Properties" : {
      "[DetectorId](#cfn-guardduty-member-detectorid)" : String,
      "[DisableEmailNotification](#cfn-guardduty-member-disableemailnotification)" : Boolean,
      "[Email](#cfn-guardduty-member-email)" : String,
      "[MemberId](#cfn-guardduty-member-memberid)" : String,
      "[Message](#cfn-guardduty-member-message)" : String,
      "[Status](#cfn-guardduty-member-status)" : String
    }
}
```

### YAML<a name="aws-resource-guardduty-member-syntax.yaml"></a>

```
Type: AWS::GuardDuty::Member
Properties: 
  [DetectorId](#cfn-guardduty-member-detectorid): String
  [DisableEmailNotification](#cfn-guardduty-member-disableemailnotification): Boolean
  [Email](#cfn-guardduty-member-email): String
  [MemberId](#cfn-guardduty-member-memberid): String
  [Message](#cfn-guardduty-member-message): String
  [Status](#cfn-guardduty-member-status): String
```

## Properties<a name="aws-resource-guardduty-member-properties"></a>

`DetectorId`  <a name="cfn-guardduty-member-detectorid"></a>
The ID of the detector associated with the GuardDuty service to add the member to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DisableEmailNotification`  <a name="cfn-guardduty-member-disableemailnotification"></a>
Specifies whether or not to disable email notification for the member account that you invite\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Email`  <a name="cfn-guardduty-member-email"></a>
The email address associated with the member account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemberId`  <a name="cfn-guardduty-member-memberid"></a>
The AWS account ID of the account to designate as a member\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Message`  <a name="cfn-guardduty-member-message"></a>
The invitation message that you want to send to the accounts that you're inviting to GuardDuty as members\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-guardduty-member-status"></a>
You can use the `Status` property to update the status of the relationship between the member account and its master account\. Valid values are `Created` and `Invited` when using an `AWS::GuardDuty::Member` resource\. If the value for this property is not provided or set to `Created`, a member account is created but not invited\. If the value of this property is set to `Invited`, a member account is created and invited\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-guardduty-member-return-values"></a>

### Ref<a name="aws-resource-guardduty-member-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique ID of the GuardDuty member account, such as 012345678901\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-guardduty-member--examples"></a>



### Declare a Member Resource<a name="aws-resource-guardduty-member--examples--Declare_a_Member_Resource"></a>

The following example shows how to declare a GuardDuty `Member` resource:

#### JSON<a name="aws-resource-guardduty-member--examples--Declare_a_Member_Resource--json"></a>

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

#### YAML<a name="aws-resource-guardduty-member--examples--Declare_a_Member_Resource--yaml"></a>

```
Type: AWS::GuardDuty::Member
Properties:
Status: Invited
MemberId: 012345678901
Email: guarddutymember@amazon.com
Message: You are invited to enable Amazon Guardduty.
DetectorId: a12abc34d567e8fa901bc2d34e56789f0
    DisableEmailNotification: true
```