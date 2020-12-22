# AWS::AuditManager::Assessment Role<a name="aws-properties-auditmanager-assessment-role"></a>

 The `Role` property type specifies the wrapper that contains AWS Audit Manager role information, such as the role type and IAM Amazon Resource Name \(ARN\)\. 

## Syntax<a name="aws-properties-auditmanager-assessment-role-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-role-syntax.json"></a>

```
{
  "[roleArn](#cfn-auditmanager-assessment-role-rolearn)" : String,
  "[roleType](#cfn-auditmanager-assessment-role-roletype)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-role-syntax.yaml"></a>

```
  [roleArn](#cfn-auditmanager-assessment-role-rolearn): String
  [roleType](#cfn-auditmanager-assessment-role-roletype): String
```

## Properties<a name="aws-properties-auditmanager-assessment-role-properties"></a>

`roleArn`  <a name="cfn-auditmanager-assessment-role-rolearn"></a>
 The Amazon Resource Name \(ARN\) of the IAM role\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:.*:iam:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`roleType`  <a name="cfn-auditmanager-assessment-role-roletype"></a>
 The type of customer persona\.   
In `CreateAssessment`, `roleType` can only be `PROCESS_OWNER`\.   
In `UpdateSettings`, `roleType` can only be `PROCESS_OWNER`\.  
In `BatchCreateDelegationByAssessment`, `roleType` can only be `RESOURCE_OWNER`\.
*Required*: No  
*Type*: String  
*Allowed values*: `PROCESS_OWNER | RESOURCE_OWNER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-role--seealso"></a>
+ [Role](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Role.html) in the *AWS Audit Manager API Reference*\.

