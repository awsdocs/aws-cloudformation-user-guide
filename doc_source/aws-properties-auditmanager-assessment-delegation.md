# AWS::AuditManager::Assessment Delegation<a name="aws-properties-auditmanager-assessment-delegation"></a>

 The `Delegation` property type specifies the assignment of a control set to a delegate for review\. 

## Syntax<a name="aws-properties-auditmanager-assessment-delegation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-delegation-syntax.json"></a>

```
{
  "[assessmentId](#cfn-auditmanager-assessment-delegation-assessmentid)" : String,
  "[assessmentName](#cfn-auditmanager-assessment-delegation-assessmentname)" : String,
  "[comment](#cfn-auditmanager-assessment-delegation-comment)" : String,
  "[controlSetId](#cfn-auditmanager-assessment-delegation-controlsetid)" : String,
  "[createdBy](#cfn-auditmanager-assessment-delegation-createdby)" : String,
  "[creationTime](#cfn-auditmanager-assessment-delegation-creationtime)" : Double,
  "[id](#cfn-auditmanager-assessment-delegation-id)" : String,
  "[lastUpdated](#cfn-auditmanager-assessment-delegation-lastupdated)" : Double,
  "[roleArn](#cfn-auditmanager-assessment-delegation-rolearn)" : String,
  "[roleType](#cfn-auditmanager-assessment-delegation-roletype)" : String,
  "[status](#cfn-auditmanager-assessment-delegation-status)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-delegation-syntax.yaml"></a>

```
  [assessmentId](#cfn-auditmanager-assessment-delegation-assessmentid): String
  [assessmentName](#cfn-auditmanager-assessment-delegation-assessmentname): String
  [comment](#cfn-auditmanager-assessment-delegation-comment): String
  [controlSetId](#cfn-auditmanager-assessment-delegation-controlsetid): String
  [createdBy](#cfn-auditmanager-assessment-delegation-createdby): String
  [creationTime](#cfn-auditmanager-assessment-delegation-creationtime): Double
  [id](#cfn-auditmanager-assessment-delegation-id): String
  [lastUpdated](#cfn-auditmanager-assessment-delegation-lastupdated): Double
  [roleArn](#cfn-auditmanager-assessment-delegation-rolearn): String
  [roleType](#cfn-auditmanager-assessment-delegation-roletype): String
  [status](#cfn-auditmanager-assessment-delegation-status): String
```

## Properties<a name="aws-properties-auditmanager-assessment-delegation-properties"></a>

`assessmentId`  <a name="cfn-auditmanager-assessment-delegation-assessmentid"></a>
 The identifier for the associated assessment\.   
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `^[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`assessmentName`  <a name="cfn-auditmanager-assessment-delegation-assessmentname"></a>
 The name of the associated assessment\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`comment`  <a name="cfn-auditmanager-assessment-delegation-comment"></a>
 The comment related to the delegation\.   
*Required*: No  
*Type*: String  
*Maximum*: `350`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`controlSetId`  <a name="cfn-auditmanager-assessment-delegation-controlsetid"></a>
 The identifier for the associated control set\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`createdBy`  <a name="cfn-auditmanager-assessment-delegation-createdby"></a>
 The IAM user or role that created the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9\s-_()\[\]]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`creationTime`  <a name="cfn-auditmanager-assessment-delegation-creationtime"></a>
 Specifies when the delegation was created\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`id`  <a name="cfn-auditmanager-assessment-delegation-id"></a>
 The unique identifier for the delegation\.   
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `^[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`lastUpdated`  <a name="cfn-auditmanager-assessment-delegation-lastupdated"></a>
 Specifies when the delegation was last updated\.   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`roleArn`  <a name="cfn-auditmanager-assessment-delegation-rolearn"></a>
 The Amazon Resource Name \(ARN\) of the IAM role\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:.*:iam:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`roleType`  <a name="cfn-auditmanager-assessment-delegation-roletype"></a>
 The type of customer persona\.   
In `CreateAssessment`, `roleType` can only be `PROCESS_OWNER`\.   
In `UpdateSettings`, `roleType` can only be `PROCESS_OWNER`\.  
In `BatchCreateDelegationByAssessment`, `roleType` can only be `RESOURCE_OWNER`\.
*Required*: No  
*Type*: String  
*Allowed values*: `PROCESS_OWNER | RESOURCE_OWNER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`status`  <a name="cfn-auditmanager-assessment-delegation-status"></a>
 The status of the delegation\.   
*Required*: No  
*Type*: String  
*Allowed values*: `COMPLETE | IN_PROGRESS | UNDER_REVIEW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-delegation--seealso"></a>
+ [Delegation](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Delegation.html) in the *AWS Audit Manager API Reference*\.

