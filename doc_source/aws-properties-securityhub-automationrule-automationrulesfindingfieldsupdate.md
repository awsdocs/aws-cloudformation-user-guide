# AWS::SecurityHub::AutomationRule AutomationRulesFindingFieldsUpdate<a name="aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate"></a>

 Identifies the finding fields that the automation rule action will update when a finding matches the defined criteria\. 

## Syntax<a name="aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate-syntax.json"></a>

```
{
  "[Confidence](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-confidence)" : Integer,
  "[Criticality](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-criticality)" : Integer,
  "[Note](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-note)" : NoteUpdate,
  "[RelatedFindings](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-relatedfindings)" : [ RelatedFinding, ... ],
  "[Severity](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-severity)" : SeverityUpdate,
  "[Types](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-types)" : [ String, ... ],
  "[UserDefinedFields](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-userdefinedfields)" : {Key: Value, ...},
  "[VerificationState](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-verificationstate)" : String,
  "[Workflow](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-workflow)" : WorkflowUpdate
}
```

### YAML<a name="aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate-syntax.yaml"></a>

```
  [Confidence](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-confidence): Integer
  [Criticality](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-criticality): Integer
  [Note](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-note): 
    NoteUpdate
  [RelatedFindings](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-relatedfindings): 
    - RelatedFinding
  [Severity](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-severity): 
    SeverityUpdate
  [Types](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-types): 
    - String
  [UserDefinedFields](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-userdefinedfields): 
    Key: Value
  [VerificationState](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-verificationstate): String
  [Workflow](#cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-workflow): 
    WorkflowUpdate
```

## Properties<a name="aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate-properties"></a>

`Confidence`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-confidence"></a>
 The rule action will update the `Confidence` field of a finding\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Criticality`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-criticality"></a>
 The rule action will update the `Criticality` field of a finding\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Note`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-note"></a>
 The rule action will update the `Note` field of a finding\.   
*Required*: No  
*Type*: [NoteUpdate](aws-properties-securityhub-automationrule-noteupdate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelatedFindings`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-relatedfindings"></a>
 The rule action will update the `RelatedFindings` field of a finding\.   
*Required*: No  
*Type*: List of [RelatedFinding](aws-properties-securityhub-automationrule-relatedfinding.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Severity`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-severity"></a>
 The rule action will update the `Severity` field of a finding\.   
*Required*: No  
*Type*: [SeverityUpdate](aws-properties-securityhub-automationrule-severityupdate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Types`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-types"></a>
 The rule action will update the `Types` field of a finding\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserDefinedFields`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-userdefinedfields"></a>
 The rule action will update the `UserDefinedFields` field of a finding\.   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerificationState`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-verificationstate"></a>
 The rule action will update the `VerificationState` field of a finding\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BENIGN_POSITIVE | FALSE_POSITIVE | TRUE_POSITIVE | UNKNOWN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Workflow`  <a name="cfn-securityhub-automationrule-automationrulesfindingfieldsupdate-workflow"></a>
 The rule action will update the `Workflow` field of a finding\.   
*Required*: No  
*Type*: [WorkflowUpdate](aws-properties-securityhub-automationrule-workflowupdate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)