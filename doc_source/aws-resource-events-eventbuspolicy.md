# AWS::Events::EventBusPolicy<a name="aws-resource-events-eventbuspolicy"></a>

Running `PutPermission` permits the specified AWS account or AWS organization to put events to the specified *event bus*\. Amazon EventBridge \(CloudWatch Events\) rules in your account are triggered by these events arriving to an event bus in your account\. 

For another account to send events to your account, that external account must have an EventBridge rule with your account's event bus as a target\.

To enable multiple AWS accounts to put events to your event bus, run `PutPermission` once for each of these accounts\. Or, if all the accounts are members of the same AWS organization, you can run `PutPermission` once specifying `Principal` as "\*" and specifying the AWS organization ID in `Condition`, to grant permissions to all accounts in that organization\.

If you grant permissions using an organization, then accounts in that organization must specify a `RoleArn` with proper permissions when they use `PutTarget` to add your account's event bus as a target\. For more information, see [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-cross-account-event-delivery.html) in the *Amazon EventBridge User Guide*\.

The permission policy on the event bus cannot exceed 10 KB in size\.

## Syntax<a name="aws-resource-events-eventbuspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-eventbuspolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Events::EventBusPolicy",
  "Properties" : {
      "[Action](#cfn-events-eventbuspolicy-action)" : String,
      "[Condition](#cfn-events-eventbuspolicy-condition)" : Condition,
      "[EventBusName](#cfn-events-eventbuspolicy-eventbusname)" : String,
      "[Principal](#cfn-events-eventbuspolicy-principal)" : String,
      "[Statement](#cfn-events-eventbuspolicy-statement)" : Json,
      "[StatementId](#cfn-events-eventbuspolicy-statementid)" : String
    }
}
```

### YAML<a name="aws-resource-events-eventbuspolicy-syntax.yaml"></a>

```
Type: AWS::Events::EventBusPolicy
Properties: 
  [Action](#cfn-events-eventbuspolicy-action): String
  [Condition](#cfn-events-eventbuspolicy-condition): 
    Condition
  [EventBusName](#cfn-events-eventbuspolicy-eventbusname): String
  [Principal](#cfn-events-eventbuspolicy-principal): String
  [Statement](#cfn-events-eventbuspolicy-statement): Json
  [StatementId](#cfn-events-eventbuspolicy-statementid): String
```

## Properties<a name="aws-resource-events-eventbuspolicy-properties"></a>

`Action`  <a name="cfn-events-eventbuspolicy-action"></a>
The action that you are enabling the other account to perform\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `events:[a-zA-Z]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Condition`  <a name="cfn-events-eventbuspolicy-condition"></a>
This parameter enables you to limit the permission to accounts that fulfill a certain condition, such as being a member of a certain AWS organization\. For more information about AWS Organizations, see [What Is AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html) in the * AWS Organizations User Guide*\.  
If you specify `Condition` with an AWS organization ID, and specify "\*" as the value for `Principal`, you grant permission to all the accounts in the named organization\.  
The `Condition` is a JSON string which must contain `Type`, `Key`, and `Value` fields\.  
*Required*: No  
*Type*: [Condition](aws-properties-events-eventbuspolicy-condition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBusName`  <a name="cfn-events-eventbuspolicy-eventbusname"></a>
The name of the event bus associated with the rule\. If you omit this, the default event bus is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-events-eventbuspolicy-principal"></a>
The 12\-digit AWS account ID that you are permitting to put events to your default event bus\. Specify "\*" to permit any account to put events to your default event bus\.  
If you specify "\*" without specifying `Condition`, avoid creating rules that may match undesirable events\. To create more secure rules, make sure that the event pattern for each rule contains an `account` field with a specific account ID from which to receive events\. Rules with an account field do not match any events sent from other accounts\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `12`  
*Pattern*: `(\d{12}|\*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statement`  <a name="cfn-events-eventbuspolicy-statement"></a>
A JSON string that describes the permission policy statement\. You can include a `Policy` parameter in the request instead of using the `StatementId`, `Action`, `Principal`, or `Condition` parameters\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatementId`  <a name="cfn-events-eventbuspolicy-statementid"></a>
An identifier string for the external account that you are granting permissions to\. If you later want to revoke the permission for this external account, specify this `StatementId` when you run [RemovePermission](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_RemovePermission.html)\.  
Each `StatementId` must be unique\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z0-9-_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-events-eventbuspolicy-return-values"></a>

### Ref<a name="aws-resource-events-eventbuspolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the event bus policy ID, such as `EventBusPolicy-1aBCdeFGh2J3`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-events-eventbuspolicy--examples"></a>



### Grant Permission to One Account<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_One_Account"></a>

The following example grants permission to one AWS account with an account ID of `111122223333`\. 

#### JSON<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_One_Account--json"></a>

```
"SampleEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "StatementId": "MyStatement",
        "Statement": {
            "Effect": "Allow",
            "Principal" : {"AWS" : "arn:aws:iam::111122223333:root"},
            "Action": "events:PutEvents",
            "Resource": "arn:aws:events:us-east-1:111122223333:event-bus/default"
        }
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_One_Account--yaml"></a>

```
SampleEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy
    Properties: 
        StatementId: "MyStatement"
        Statement: 
            Effect: "Allow"
            Principal: 
                AWS: "arn:aws:iam::111122223333:root"
            Action: "events:PutEvents"
            Resource: "arn:aws:events:us-east-1:111122223333:event-bus/default"
```

### Grant Permission to an Organization<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization"></a>

The following example grants permission to all AWS accounts in the organization with an organization ID of `o-1234567890`\.

#### JSON<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization--json"></a>

```
"SampleEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "StatementId": "MyStatement",
        "Statement": {
            "Effect": "Allow",
            "Principal" : "*",
            "Action": "events:PutEvents",
            "Resource": "arn:aws:events:us-east-1:111122223333:event-bus/default",
            "Condition": {
                "StringEquals": {"aws:PrincipalOrgID": "o-1234567890"}
             }
        }
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization--yaml"></a>

```
SampleEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy
    Properties: 
        StatementId: "MyStatement"
        Statement: 
            Effect: "Allow"
            Principal: "*"
            Action: "events:PutEvents"
            Resource: "arn:aws:events:us-east-1:111122223333:event-bus/default"
            Condition:
                StringEquals:
                    "aws:PrincipalOrgID": "o-1234567890"
```

### Deny policy using multiple principals and actions<a name="aws-resource-events-eventbuspolicy--examples--Deny_policy_using_multiple_principals_and_actions"></a>

The following example demonstrates a deny policy statement using multiple principals and actions\.

#### JSON<a name="aws-resource-events-eventbuspolicy--examples--Deny_policy_using_multiple_principals_and_actions--json"></a>

```
"SampleDenyEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "StatementId": "MyDenyStatement",
        "Statement": {
            "Effect": "Deny",
            "Principal" : 
                {"AWS" : ["arn:aws:iam::111122223333:user/alice", "arn:aws:iam::111122223333:user/bob"]},
            "Action": [
                "events:PutEvents",
                "events:PutRule"
            ],
            "Resource": "arn:aws:events:us-east-1:111122223333:event-bus/default"
        }
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy--examples--Deny_policy_using_multiple_principals_and_actions--yaml"></a>

```
SampleDenyEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy
    Properties: 
        StatementId: "MyDenyStatement"
        Statement: 
            Effect: "Deny"
            Principal: 
                AWS: 
                    - "arn:aws:iam::111122223333:user/alice"
                    - "arn:aws:iam::111122223333:user/bob"
            Action: 
                - "events:PutEvents"
                - "events:PutRule"
            Resource: "arn:aws:events:us-east-1:111122223333:event-bus/default"
```

### Grant Permission to an Organization using a custom event bus<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization_using_a_custom_event_bus"></a>

The following example grants permission to all AWS accounts in the organization with an organization ID of `o-1234567890` using a custom event bus\.

#### JSON<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization_using_a_custom_event_bus--json"></a>

```
"SampleCustomEventBus": {
    "Type": "AWS::Events::EventBus",
    "Properties": {
        "Name": "MyCustomEventBus"
     }
},
"SampleCustomEventBusPolicy": {
    "Type": "AWS::Events::EventBusPolicy",
    "Properties": {
        "EventBusName": {
            "Ref": "SampleCustomEventBus"
        },
        "StatementId": "MyCustomEventBusStatement",
        "Statement": {
            "Effect": "Allow",
            "Principal" : "*",
            "Action": "events:PutEvents",
            "Resource": {
                "Fn::GetAtt": [
                    "SampleCustomEventBus",
                    "Arn"
                ]
            },
            "Condition": {
                "StringEquals": {"aws:PrincipalOrgID": "o-1234567890"}
            }
        }
    }
}
```

#### YAML<a name="aws-resource-events-eventbuspolicy--examples--Grant_Permission_to_an_Organization_using_a_custom_event_bus--yaml"></a>

```
SampleCustomEventBus: 
    Type: AWS::Events::EventBus
    Properties:
        Name: "MyCustomEventBus"

SampleCustomEventBusPolicy: 
    Type: AWS::Events::EventBusPolicy
    Properties: 
        EventBusName:
            Ref: "SampleCustomEventBus"
        StatementId: "MyCustomEventBusStatement"
        Statement:
            Effect: "Allow"
            Principal: "*"
            Action: "events:PutEvents"
            Resource: !GetAtt "SampleCustomEventBus.Arn"
            Condition:
                StringEquals:
                    "aws:PrincipalOrgID": "o-1234567890"
```