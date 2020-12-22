# AWS::AuditManager::Assessment Tags<a name="aws-properties-auditmanager-assessment-tags"></a>

The `Tags` property type specifies the tags associated with the assessment\.

## Syntax<a name="aws-properties-auditmanager-assessment-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-tags-syntax.json"></a>

```
{
  "[Tags](#cfn-auditmanager-assessment-tags-tags)" : [ Tag, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-tags-syntax.yaml"></a>

```
  [Tags](#cfn-auditmanager-assessment-tags-tags): 
    - Tag
```

## Properties<a name="aws-properties-auditmanager-assessment-tags-properties"></a>

`Tags`  <a name="cfn-auditmanager-assessment-tags-tags"></a>
The list of tags associated with the assessment\.  
*Required*: No  
*Type*: [List](#aws-properties-auditmanager-assessment-tags) of [Tag](#aws-properties-auditmanager-assessment-tags)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-tags--seealso"></a>
+ [Tags](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_CreateAssessment.html#auditmanager-CreateAssessment-request-tags) in the *AWS Audit Manager API Reference*\.

