# AWS::GuardDuty::Master<a name="aws-resource-guardduty-master"></a>

You can use the `AWS::GuardDuty::Master` resource in a GuardDuty member account to accept an invitation from a GuardDuty master account\. The invitation to the member account must be sent prior to using the `AWS::GuardDuty::Master` resource to accept the master account's invitation\. You can invite a member account by using the `InviteMembers` operation of the Amazon GuardDuty API, or by creating an `AWS::GuardDuty::Member` resource\.

## Syntax<a name="aws-resource-guardduty-master-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-master-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Master",
  "Properties" : {
      "[DetectorId](#cfn-guardduty-master-detectorid)" : String,
      "[InvitationId](#cfn-guardduty-master-invitationid)" : String,
      "[MasterId](#cfn-guardduty-master-masterid)" : String
    }
}
```

### YAML<a name="aws-resource-guardduty-master-syntax.yaml"></a>

```
Type: AWS::GuardDuty::Master
Properties: 
  [DetectorId](#cfn-guardduty-master-detectorid): String
  [InvitationId](#cfn-guardduty-master-invitationid): String
  [MasterId](#cfn-guardduty-master-masterid): String
```

## Properties<a name="aws-resource-guardduty-master-properties"></a>

`DetectorId`  <a name="cfn-guardduty-master-detectorid"></a>
The unique ID of the detector of the GuardDuty member account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InvitationId`  <a name="cfn-guardduty-master-invitationid"></a>
The ID of the invitation that is sent to the account designated as a member account\. You can find the invitation ID by using the ListInvitation action of the GuardDuty API\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterId`  <a name="cfn-guardduty-master-masterid"></a>
The AWS account ID of the account designated as the GuardDuty master account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-guardduty-master-return-values"></a>

### Ref<a name="aws-resource-guardduty-master-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique ID of the GuardDuty master account, such as 012345678901\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-guardduty-master--examples"></a>



### Declare a Master Resource<a name="aws-resource-guardduty-master--examples--Declare_a_Master_Resource"></a>

To declare a GuardDuty `Master` resource:

#### JSON<a name="aws-resource-guardduty-master--examples--Declare_a_Master_Resource--json"></a>

```
"GDMaster": {
    "Type" : "AWS::GuardDuty::Master",
    "Properties" : {
        "DetectorId" : "a12abc34d567e8fa901bc2d34e56789f0",
        "MasterId" : "012345678901",
        "InvitationId" : "84b097800250d17d1872b34c4daadcf5"
    }
}
```

#### YAML<a name="aws-resource-guardduty-master--examples--Declare_a_Master_Resource--yaml"></a>

```
GDMaster:
    Type: AWS::GuardDuty::Master
    Properties:
        DetectorId: "a12abc34d567e8fa901bc2d34e56789f0"
        MasterId: "012345678901"
        InvitationId: "84b097800250d17d1872b34c4daadcf5"
```