# AWS::Detective::MemberInvitation<a name="aws-resource-detective-memberinvitation"></a>

The `AWS::Detective::MemberInvitation` resource is an Amazon Detective resource type that sends an invitation to join a Detective behavior graph\. The invitation is sent from the master account to the root user email address of an AWS account\.

## Syntax<a name="aws-resource-detective-memberinvitation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-detective-memberinvitation-syntax.json"></a>

```
{
  "Type" : "AWS::Detective::MemberInvitation",
  "Properties" : {
      "[GraphArn](#cfn-detective-memberinvitation-grapharn)" : String,
      "[MemberEmailAddress](#cfn-detective-memberinvitation-memberemailaddress)" : String,
      "[MemberId](#cfn-detective-memberinvitation-memberid)" : String,
      "[Message](#cfn-detective-memberinvitation-message)" : String
    }
}
```

### YAML<a name="aws-resource-detective-memberinvitation-syntax.yaml"></a>

```
Type: AWS::Detective::MemberInvitation
Properties: 
  [GraphArn](#cfn-detective-memberinvitation-grapharn): String
  [MemberEmailAddress](#cfn-detective-memberinvitation-memberemailaddress): String
  [MemberId](#cfn-detective-memberinvitation-memberid): String
  [Message](#cfn-detective-memberinvitation-message): String
```

## Properties<a name="aws-resource-detective-memberinvitation-properties"></a>

`GraphArn`  <a name="cfn-detective-memberinvitation-grapharn"></a>
The ARN of the behavior graph to invite the account to contribute data to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemberEmailAddress`  <a name="cfn-detective-memberinvitation-memberemailaddress"></a>
The root user email address of the invited account\. If the email address provided is not the root user email address for the provided account, the invitation creation fails\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemberId`  <a name="cfn-detective-memberinvitation-memberid"></a>
The AWS account identifier of the invited account  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Message`  <a name="cfn-detective-memberinvitation-message"></a>
Customized text to include in the invitation email message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-detective-memberinvitation-return-values"></a>

### Ref<a name="aws-resource-detective-memberinvitation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the behavior graph and the member account identifier, separated by a pipe character \('\|'\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-detective-memberinvitation--examples"></a>

### Sending a behavior graph invitation to a member account<a name="aws-resource-detective-memberinvitation--examples--Sending_a_behavior_graph_invitation_to_a_member_account"></a>

This example shows how to declare a new `AWS:Detective:MemberInvitation` resource to create a new invitation to a member account\.

#### JSON<a name="aws-resource-detective-memberinvitation--examples--Sending_a_behavior_graph_invitation_to_a_member_account--json"></a>

```
"MemberInvitation": {
    "Type": "AWS::Detective::MemberInvitation",
    "Properties": {
        "GraphArn": "arn:aws:detective:us-east-1:111122223333:graph:027c7c4610ea4aacaf0b883093cab899",
        "MemberId": "444455556666",
        "MemberEmailAddress": "mmajor@example.com",
        "Message": "This is Paul Santos. I need to add your account to the data we use for security investigation in Detective. If you have any questions, contact me at psantos@example.com."
     }
}
```

#### YAML<a name="aws-resource-detective-memberinvitation--examples--Sending_a_behavior_graph_invitation_to_a_member_account--yaml"></a>

```
MemberInvitation:
    Type: AWS::Detective::MemberInvitation
    Properties:
      GraphArn: "arn:aws:detective:us-east-1:111122223333:graph:027c7c4610ea4aacaf0b883093cab899"
      MemberId: 444455556666
      MemberEmailAddress: mmajor@example.com
      Message: This is Paul Santos. I need to add your account to the data we use for security investigation in Detective. If you have any questions, contact me at psantos@example.com.
```