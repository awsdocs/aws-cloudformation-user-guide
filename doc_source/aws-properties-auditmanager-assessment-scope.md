# AWS::AuditManager::Assessment Scope<a name="aws-properties-auditmanager-assessment-scope"></a>

The `Scope` property type specifies the wrapper that contains the AWS accounts and services that are in scope for the assessment\.

## Syntax<a name="aws-properties-auditmanager-assessment-scope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-scope-syntax.json"></a>

```
{
  "[AwsAccounts](#cfn-auditmanager-assessment-scope-awsaccounts)" : [ AWSAccount, ... ],
  "[AwsServices](#cfn-auditmanager-assessment-scope-awsservices)" : [ AWSService, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-scope-syntax.yaml"></a>

```
  [AwsAccounts](#cfn-auditmanager-assessment-scope-awsaccounts): 
    - AWSAccount
  [AwsServices](#cfn-auditmanager-assessment-scope-awsservices): 
    - AWSService
```

## Properties<a name="aws-properties-auditmanager-assessment-scope-properties"></a>

`AwsAccounts`  <a name="cfn-auditmanager-assessment-scope-awsaccounts"></a>
 The AWS accounts that are included in the scope of the assessment\.   
*Required*: No  
*Type*: List of [AWSAccount](aws-properties-auditmanager-assessment-awsaccount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsServices`  <a name="cfn-auditmanager-assessment-scope-awsservices"></a>
 The AWS services that are included in the scope of the assessment\.   
*Required*: No  
*Type*: List of [AWSService](aws-properties-auditmanager-assessment-awsservice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-scope--seealso"></a>
+ [Scope](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Scope.html) in the *AWS Audit Manager API Reference*\.

