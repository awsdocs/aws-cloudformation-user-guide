# AWS::AuditManager::Assessment AWSServices<a name="aws-properties-auditmanager-assessment-awsservices"></a>

The `AWSServices` property type specifies the AWS services in scope, such as Amazon S3, AWS CloudTrail, and so on\.

## Syntax<a name="aws-properties-auditmanager-assessment-awsservices-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-awsservices-syntax.json"></a>

```
{
  "[AWSServices](#cfn-auditmanager-assessment-awsservices-awsservices)" : [ AWSService, ... ]
}
```

### YAML<a name="aws-properties-auditmanager-assessment-awsservices-syntax.yaml"></a>

```
  [AWSServices](#cfn-auditmanager-assessment-awsservices-awsservices): 
    - AWSService
```

## Properties<a name="aws-properties-auditmanager-assessment-awsservices-properties"></a>

`AWSServices`  <a name="cfn-auditmanager-assessment-awsservices-awsservices"></a>
The list of AWS services in scope for the assessment\.  
*Required*: No  
*Type*: [List](#aws-properties-auditmanager-assessment-awsservices) of [AWSService](aws-properties-auditmanager-assessment-awsservice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-awsservices--seealso"></a>
+ [AWSService](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_AWSService.html) in the *AWS Audit Manager API Reference*\.

