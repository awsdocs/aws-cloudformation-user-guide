# AWS::AuditManager::Assessment Delegation<a name="aws-properties-auditmanager-assessment-delegation"></a>

The `Delegation` property type specifies the assignment of a control set to a delegate for review\.

## Syntax<a name="aws-properties-auditmanager-assessment-delegation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-delegation-syntax.json"></a>

```
{
  "[AssessmentId](#cfn-auditmanager-assessment-delegation-assessmentid)" : String,
  "[AssessmentName](#cfn-auditmanager-assessment-delegation-assessmentname)" : String,
  "[Comment](#cfn-auditmanager-assessment-delegation-comment)" : String,
  "[ControlSetId](#cfn-auditmanager-assessment-delegation-controlsetid)" : String,
  "[CreatedBy](#cfn-auditmanager-assessment-delegation-createdby)" : String,
  "[CreationTime](#cfn-auditmanager-assessment-delegation-creationtime)" : Double,
  "[Id](#cfn-auditmanager-assessment-delegation-id)" : String,
  "[LastUpdated](#cfn-auditmanager-assessment-delegation-lastupdated)" : Double,
  "[RoleArn](#cfn-auditmanager-assessment-delegation-rolearn)" : String,
  "[RoleType](#cfn-auditmanager-assessment-delegation-roletype)" : String,
  "[Status](#cfn-auditmanager-assessment-delegation-status)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-delegation-syntax.yaml"></a>

```
  [AssessmentId](#cfn-auditmanager-assessment-delegation-assessmentid): String
  [AssessmentName](#cfn-auditmanager-assessment-delegation-assessmentname): String
  [Comment](#cfn-auditmanager-assessment-delegation-comment): String
  [ControlSetId](#cfn-auditmanager-assessment-delegation-controlsetid): String
  [CreatedBy](#cfn-auditmanager-assessment-delegation-createdby): String
  [CreationTime](#cfn-auditmanager-assessment-delegation-creationtime): Double
  [Id](#cfn-auditmanager-assessment-delegation-id): String
  [LastUpdated](#cfn-auditmanager-assessment-delegation-lastupdated): Double
  [RoleArn](#cfn-auditmanager-assessment-delegation-rolearn): String
  [RoleType](#cfn-auditmanager-assessment-delegation-roletype): String
  [Status](#cfn-auditmanager-assessment-delegation-status): String
```

## Properties<a name="aws-properties-auditmanager-assessment-delegation-properties"></a>

`AssessmentId`  <a name="cfn-auditmanager-assessment-delegation-assessmentid"></a>
 The identifier for the assessment that's associated with the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `^[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssessmentName`  <a name="cfn-auditmanager-assessment-delegation-assessmentname"></a>
 The name of the assessment that's associated with the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[^\\]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-auditmanager-assessment-delegation-comment"></a>
 The comment that's related to the delegation\.   
*Required*: No  
*Type*: String  
*Maximum*: `350`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ControlSetId`  <a name="cfn-auditmanager-assessment-delegation-controlsetid"></a>
 The identifier for the control set that's associated with the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedBy`  <a name="cfn-auditmanager-assessment-delegation-createdby"></a>
 The user or role that created the delegation\.  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9-_()\\[\\]\\s]+$`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreationTime`  <a name="cfn-auditmanager-assessment-delegation-creationtime"></a>
 Specifies when the delegation was created\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-auditmanager-assessment-delegation-id"></a>
 The unique identifier for the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `^[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastUpdated`  <a name="cfn-auditmanager-assessment-delegation-lastupdated"></a>
 Specifies when the delegation was last updated\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-auditmanager-assessment-delegation-rolearn"></a>
 The Amazon Resource Name \(ARN\) of the IAM role\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:.*:iam:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleType`  <a name="cfn-auditmanager-assessment-delegation-roletype"></a>
 The type of customer persona\.   
In `CreateAssessment`, `roleType` can only be `PROCESS_OWNER`\.   
In `UpdateSettings`, `roleType` can only be `PROCESS_OWNER`\.  
In `BatchCreateDelegationByAssessment`, `roleType` can only be `RESOURCE_OWNER`\.
*Required*: No  
*Type*: String  
*Allowed values*: `PROCESS_OWNER | RESOURCE_OWNER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-auditmanager-assessment-delegation-status"></a>
 The status of the delegation\.   
*Required*: No  
*Type*: String  
*Allowed values*: `COMPLETE | IN_PROGRESS | UNDER_REVIEW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-delegation--seealso"></a>
+ [Delegation](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Delegation.html) in the *AWS Audit Manager API Reference*\.

