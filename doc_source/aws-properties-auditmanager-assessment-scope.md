# AWS::AuditManager::Assessment Scope<a name="aws-properties-auditmanager-assessment-scope"></a>

 The `Scope` property type specifies the wrapper that contains the AWS accounts and AWS services in scope for the assessment\. 

## Syntax<a name="aws-properties-auditmanager-assessment-scope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-scope-syntax.json"></a>

```
{
  "[awsAccounts](#cfn-auditmanager-assessment-scope-awsaccounts)" : AWSAccounts,
  "[awsServices](#cfn-auditmanager-assessment-scope-awsservices)" : AWSServices
}
```

### YAML<a name="aws-properties-auditmanager-assessment-scope-syntax.yaml"></a>

```
  [awsAccounts](#cfn-auditmanager-assessment-scope-awsaccounts): 
    AWSAccounts
  [awsServices](#cfn-auditmanager-assessment-scope-awsservices): 
    AWSServices
```

## Properties<a name="aws-properties-auditmanager-assessment-scope-properties"></a>

`awsAccounts`  <a name="cfn-auditmanager-assessment-scope-awsaccounts"></a>
 The AWS accounts included in the scope of the assessment\.   
*Required*: No  
*Type*: [AWSAccounts](aws-properties-auditmanager-assessment-awsaccounts.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`awsServices`  <a name="cfn-auditmanager-assessment-scope-awsservices"></a>
 The AWS services included in the scope of the assessment\.   
*Required*: No  
*Type*: [AWSServices](aws-properties-auditmanager-assessment-awsservices.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-scope--seealso"></a>
+ [Scope](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Scope.html) in the *AWS Audit Manager API Reference*\.

