# AWS::AuditManager::Assessment Roles<a name="aws-properties-auditmanager-assessment-roles"></a>

The `Roles` property type specifies the roles associated with the assessment\.

## Syntax<a name="aws-properties-auditmanager-assessment-roles-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-roles-syntax.json"></a>

```
{
  "[Roles](#cfn-auditmanager-assessment-roles-roles)" : [ Role, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-roles-syntax.yaml"></a>

```
  [Roles](#cfn-auditmanager-assessment-roles-roles): 
    - Role
```

## Properties<a name="aws-properties-auditmanager-assessment-roles-properties"></a>

`Roles`  <a name="cfn-auditmanager-assessment-roles-roles"></a>
The list of roles associated with the assessment\.  
*Required*: No  
*Type*: [List](#aws-properties-auditmanager-assessment-roles) of [Role](aws-properties-auditmanager-assessment-role.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-roles--seealso"></a>
+ [Role](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_Role.html) in the *AWS Audit Manager API Reference*\.

