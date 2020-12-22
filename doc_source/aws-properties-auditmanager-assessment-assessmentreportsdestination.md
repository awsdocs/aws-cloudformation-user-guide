# AWS::AuditManager::Assessment AssessmentReportsDestination<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination"></a>

 The `AssessmentReportsDestination` property type specifies the location in which AWS Audit Manager saves assessment reports for the given assessment\. 

## Syntax<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination-syntax.json"></a>

```
{
  "[destination](#cfn-auditmanager-assessment-assessmentreportsdestination-destination)" : String,
  "[destinationType](#cfn-auditmanager-assessment-assessmentreportsdestination-destinationtype)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination-syntax.yaml"></a>

```
  [destination](#cfn-auditmanager-assessment-assessmentreportsdestination-destination): String
  [destinationType](#cfn-auditmanager-assessment-assessmentreportsdestination-destinationtype): String
```

## Properties<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination-properties"></a>

`destination`  <a name="cfn-auditmanager-assessment-assessmentreportsdestination-destination"></a>
 The destination of the assessment report\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^(S|s)3:\/\/[a-zA-Z0-9-_\/.]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`destinationType`  <a name="cfn-auditmanager-assessment-assessmentreportsdestination-destinationtype"></a>
 The destination type, such as Amazon S3\.   
*Required*: No  
*Type*: String  
*Allowed values*: `S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-auditmanager-assessment-assessmentreportsdestination--seealso"></a>
+ [AssessmentReportsDestination](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_AssessmentReportsDestination.html) in the *AWS Audit Manager API Reference*\.

