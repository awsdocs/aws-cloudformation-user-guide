# AWS::StepFunctions::StateMachineVersion<a name="aws-resource-stepfunctions-statemachineversion"></a>

Represents a state machine [version](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-state-machine-version.html)\. A published version uses the latest state machine [https://docs.aws.amazon.com/step-functions/latest/dg/concepts-state-machine-version.html](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-state-machine-version.html)\. A revision is an immutable, read\-only snapshot of a state machine’s definition and configuration\.

You can publish up to 1000 versions for each state machine\.

**Important**  
Before you delete a version, make sure that version's ARN isn't being referenced in any long\-running workflows or application code outside of the stack\.

## Syntax<a name="aws-resource-stepfunctions-statemachineversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-stepfunctions-statemachineversion-syntax.json"></a>

```
{
  "Type" : "AWS::StepFunctions::StateMachineVersion",
  "Properties" : {
      "[Description](#cfn-stepfunctions-statemachineversion-description)" : String,
      "[StateMachineArn](#cfn-stepfunctions-statemachineversion-statemachinearn)" : String,
      "[StateMachineRevisionId](#cfn-stepfunctions-statemachineversion-statemachinerevisionid)" : String
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachineversion-syntax.yaml"></a>

```
Type: AWS::StepFunctions::StateMachineVersion
Properties: 
  [Description](#cfn-stepfunctions-statemachineversion-description): String
  [StateMachineArn](#cfn-stepfunctions-statemachineversion-statemachinearn): String
  [StateMachineRevisionId](#cfn-stepfunctions-statemachineversion-statemachinerevisionid): String
```

## Properties<a name="aws-resource-stepfunctions-statemachineversion-properties"></a>

`Description`  <a name="cfn-stepfunctions-statemachineversion-description"></a>
An optional description of the state machine version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateMachineArn`  <a name="cfn-stepfunctions-statemachineversion-statemachinearn"></a>
The Amazon Resource Name \(ARN\) of the state machine\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StateMachineRevisionId`  <a name="cfn-stepfunctions-statemachineversion-statemachinerevisionid"></a>
Identifier for a state machine revision, which is an immutable, read\-only snapshot of a state machine’s definition and configuration\.  
Only publish the state machine version if the current state machine's revision ID matches the specified ID\. Use this option to avoid publishing a version if the state machine has changed since you last updated it\.  
To specify the initial state machine revision, set the value as `INITIAL`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-stepfunctions-statemachineversion-return-values"></a>

### Ref<a name="aws-resource-stepfunctions-statemachineversion-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the published state machine version\. For example, `arn:aws:states:us-east-1:123456789012:stateMachine:myStateMachine:1.`

For more information about using `Ref`, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-statemachineversion-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following is the available attribute\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-stepfunctions-statemachineversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the ARN of the state machine version\. For example, `arn:aws:states:us-east-1:123456789012:stateMachine:myStateMachine:1`\.

## Examples<a name="aws-resource-stepfunctions-statemachineversion--examples"></a>

The following example shows how you can create multiple versions of the same state machine with a CloudFormation template\.

### Publish multiple state machine versions<a name="aws-resource-stepfunctions-statemachineversion--examples--Publish_multiple_state_machine_versions"></a>

#### YAML<a name="aws-resource-stepfunctions-statemachineversion--examples--Publish_multiple_state_machine_versions--yaml"></a>

```
MyStateMachineVersionA:
  Type: AWS::StepFunctions::StateMachineVersion
  Properties:
    Description: Version 1
    StateMachineArn: !Ref MyStateMachine

MyStateMachineVersionB:
  Type: AWS::StepFunctions::StateMachineVersion
  Properties:
    Description: Version 2
    StateMachineArn: !Ref MyStateMachine
```