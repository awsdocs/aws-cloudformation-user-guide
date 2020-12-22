# AWS::AuditManager::Assessment AWSAccounts<a name="aws-properties-auditmanager-assessment-awsaccounts"></a>

 The `AWSAccounts` property type specifies the AWS accounts in scope\. 

## Syntax<a name="aws-properties-auditmanager-assessment-awsaccounts-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-awsaccounts-syntax.json"></a>

```
{
  "[AWSAccounts](#cfn-auditmanager-assessment-awsaccounts-awsaccounts)" : [ AWSAccount, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-awsaccounts-syntax.yaml"></a>

```
  [AWSAccounts](#cfn-auditmanager-assessment-awsaccounts-awsaccounts): 
    - AWSAccount
```

## Properties<a name="aws-properties-auditmanager-assessment-awsaccounts-properties"></a>

`AWSAccounts`  <a name="cfn-auditmanager-assessment-awsaccounts-awsaccounts"></a>
The list of AWS accounts in scope\.  
*Required*: No  
*Type*: [List](#aws-properties-auditmanager-assessment-awsaccounts) of [AWSAccount](aws-properties-auditmanager-assessment-awsaccount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-awsaccounts--seealso"></a>
+ [AWSAccount](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_AWSAccount.html) in the *AWS Audit Manager API Reference*\.

