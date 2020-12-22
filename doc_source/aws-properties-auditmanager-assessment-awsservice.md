# AWS::AuditManager::Assessment AWSService<a name="aws-properties-auditmanager-assessment-awsservice"></a>

 The `AWSService` property type specifies an AWS service such as Amazon S3, AWS CloudTrail, and so on\. 

## Syntax<a name="aws-properties-auditmanager-assessment-awsservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-awsservice-syntax.json"></a>

```
{
  "[serviceName](#cfn-auditmanager-assessment-awsservice-servicename)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-awsservice-syntax.yaml"></a>

```
  [serviceName](#cfn-auditmanager-assessment-awsservice-servicename): String
```

## Properties<a name="aws-properties-auditmanager-assessment-awsservice-properties"></a>

`serviceName`  <a name="cfn-auditmanager-assessment-awsservice-servicename"></a>
 The name of the AWS service\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `40`  
*Pattern*: `^[a-zA-Z0-9-\s().]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-awsservice--seealso"></a>
+ [AWSService](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_AWSService.html) in the *AWS Audit Manager API Reference*\.

