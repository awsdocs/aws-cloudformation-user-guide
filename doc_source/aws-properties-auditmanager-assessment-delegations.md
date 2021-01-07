# AWS::AuditManager::Assessment Delegations<a name="aws-properties-auditmanager-assessment-delegations"></a>

 The `Delegations` property type specifies the delegations for the assessment\. 

## Syntax<a name="aws-properties-auditmanager-assessment-delegations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-delegations-syntax.json"></a>

```
{
  "[Delegations](#cfn-auditmanager-assessment-delegations-delegations)" : [ Delegation, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-delegations-syntax.yaml"></a>

```
  [Delegations](#cfn-auditmanager-assessment-delegations-delegations): 
    - Delegation
```

## Properties<a name="aws-properties-auditmanager-assessment-delegations-properties"></a>

`Delegations`  <a name="cfn-auditmanager-assessment-delegations-delegations"></a>
The list of delegations for the assessment\.  
*Required*: No  
*Type*: [List](#aws-properties-auditmanager-assessment-delegations) of [Delegation](aws-properties-auditmanager-assessment-delegation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-delegations--seealso"></a>
+ [Delegation](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Delegation.html) in the *AWS Audit Manager API Reference*\.

