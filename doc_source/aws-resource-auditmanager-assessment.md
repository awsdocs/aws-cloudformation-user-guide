# AWS::AuditManager::Assessment<a name="aws-resource-auditmanager-assessment"></a>

 The `AWS::AuditManager::Assessment` resource is an AWS Audit Manager resource type that defines the scope of audit evidence collected by AWS Audit Manager\. An AWS Audit Manager assessment is an implementation of an AWS Audit Manager framework\. 

## Syntax<a name="aws-resource-auditmanager-assessment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-auditmanager-assessment-syntax.json"></a>

```
{
  "Type" : "AWS::AuditManager::Assessment",
  "Properties" : {
      "[assessmentReportsDestination](#cfn-auditmanager-assessment-assessmentreportsdestination)" : AssessmentReportsDestination,
      "[awsAccount](#cfn-auditmanager-assessment-awsaccount)" : AWSAccount,
      "[description](#cfn-auditmanager-assessment-description)" : String,
      "[frameworkId](#cfn-auditmanager-assessment-frameworkid)" : String,
      "[name](#cfn-auditmanager-assessment-name)" : String,
      "[roles](#cfn-auditmanager-assessment-roles)" : Roles,
      "[scope](#cfn-auditmanager-assessment-scope)" : Scope,
      "[status](#cfn-auditmanager-assessment-status)" : String,
      "[tags](#cfn-auditmanager-assessment-tags)" : Tags
    }
}
```

### YAML<a name="aws-resource-auditmanager-assessment-syntax.yaml"></a>

```
Type: AWS::AuditManager::Assessment
Properties: 
  [assessmentReportsDestination](#cfn-auditmanager-assessment-assessmentreportsdestination): 
    AssessmentReportsDestination
  [awsAccount](#cfn-auditmanager-assessment-awsaccount): 
    AWSAccount
  [description](#cfn-auditmanager-assessment-description): String
  [frameworkId](#cfn-auditmanager-assessment-frameworkid): String
  [name](#cfn-auditmanager-assessment-name): String
  [roles](#cfn-auditmanager-assessment-roles): 
    Roles
  [scope](#cfn-auditmanager-assessment-scope): 
    Scope
  [status](#cfn-auditmanager-assessment-status): String
  [tags](#cfn-auditmanager-assessment-tags): 
    Tags
```

## Properties<a name="aws-resource-auditmanager-assessment-properties"></a>

`assessmentReportsDestination`  <a name="cfn-auditmanager-assessment-assessmentreportsdestination"></a>
 The destination in which evidence reports are stored for the specified assessment\.   
*Required*: No  
*Type*: [AssessmentReportsDestination](aws-properties-auditmanager-assessment-assessmentreportsdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`awsAccount`  <a name="cfn-auditmanager-assessment-awsaccount"></a>
 The AWS account associated with the assessment\.   
*Required*: No  
*Type*: [AWSAccount](aws-properties-auditmanager-assessment-awsaccount.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`description`  <a name="cfn-auditmanager-assessment-description"></a>
 The description of the assessment\.   
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`frameworkId`  <a name="cfn-auditmanager-assessment-frameworkid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`name`  <a name="cfn-auditmanager-assessment-name"></a>
 The name of the assessment\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`roles`  <a name="cfn-auditmanager-assessment-roles"></a>
 The roles associated with the assessment\.   
*Required*: No  
*Type*: [Roles](aws-properties-auditmanager-assessment-roles.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`scope`  <a name="cfn-auditmanager-assessment-scope"></a>
 The wrapper of AWS accounts and services in scope for the assessment\.   
*Required*: No  
*Type*: [Scope](aws-properties-auditmanager-assessment-scope.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`status`  <a name="cfn-auditmanager-assessment-status"></a>
 The overall status of the assessment\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ACTIVE | INACTIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`tags`  <a name="cfn-auditmanager-assessment-tags"></a>
 The tags associated with the assessment\.   
*Required*: No  
*Type*: [Tags](aws-properties-auditmanager-assessment-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-auditmanager-assessment-return-values"></a>

### Ref<a name="aws-resource-auditmanager-assessment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the assessment ID\. For example:

            `{ "Ref": "111A1A1A-22B2-33C3-DDD4-55E5E5E555E5" }`        

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-auditmanager-assessment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-auditmanager-assessment-return-values-fn--getatt-fn--getatt"></a>

`arn`  <a name="arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the assessment\. For example, `arn:aws:auditmanager:us-east-1:123456789012:assessment/111A1A1A-22B2-33C3-DDD4-55E5E5E555E5`\. 

`assessmentId`  <a name="assessmentId-fn::getatt"></a>
The unique identifier for the assessment\. For example, `111A1A1A-22B2-33C3-DDD4-55E5E5E555E5`\.

`creationTime`  <a name="creationTime-fn::getatt"></a>
The time when the assessment was created\. For example, `1607582033.373`\.

`delegations`  <a name="delegations-fn::getatt"></a>
The delegations associated with the assessment\. For example:  

```
[ {
"assessmentId" : null,
"assessmentName" : null,
"comment" : null,
"controlSetId" : "CloudTrail Checks",
"createdBy" : "arn:aws:sts::123456789012:assumed-role/Admin/JohnDoe",
"creationTime" : 1.607671498292E9,
"id" : "aaaa1111-bb22-cc33-dd44-eeeeee555555",
"lastUpdated" : 1.607671498292E9,
"roleArn" : "arn:aws:iam::123456789012:user/JohnDoe",
"roleType" : "RESOURCE_OWNER",
"status" : "IN_PROGRESS"
} ]
```

`frameworkId`  <a name="frameworkId-fn::getatt"></a>
The unique identifier for the framework\. For example, `1aaa1111-22b2-33c3-3333-d44dd4d444dd`\.

## See also<a name="aws-resource-auditmanager-assessment--seealso"></a>
+ [CreateAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_CreateAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [DeleteAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [GetAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_GetAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [UpdateAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_UpdateAssessment.html) in the *AWS Audit Manager API Reference*\.

