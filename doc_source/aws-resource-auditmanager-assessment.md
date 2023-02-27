# AWS::AuditManager::Assessment<a name="aws-resource-auditmanager-assessment"></a>

The `AWS::AuditManager::Assessment` resource is an Audit Manager resource type that defines the scope of audit evidence collected by Audit Manager\. An Audit Manager assessment is an implementation of an Audit Manager framework\. 

## Syntax<a name="aws-resource-auditmanager-assessment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-auditmanager-assessment-syntax.json"></a>

```
{
  "Type" : "AWS::AuditManager::Assessment",
  "Properties" : {
      "[AssessmentReportsDestination](#cfn-auditmanager-assessment-assessmentreportsdestination)" : AssessmentReportsDestination,
      "[AwsAccount](#cfn-auditmanager-assessment-awsaccount)" : AWSAccount,
      "[Delegations](#cfn-auditmanager-assessment-delegations)" : [ Delegation, ... ],
      "[Description](#cfn-auditmanager-assessment-description)" : String,
      "[FrameworkId](#cfn-auditmanager-assessment-frameworkid)" : String,
      "[Name](#cfn-auditmanager-assessment-name)" : String,
      "[Roles](#cfn-auditmanager-assessment-roles)" : [ Role, ... ],
      "[Scope](#cfn-auditmanager-assessment-scope)" : Scope,
      "[Status](#cfn-auditmanager-assessment-status)" : String,
      "[Tags](#cfn-auditmanager-assessment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-auditmanager-assessment-syntax.yaml"></a>

```
Type: AWS::AuditManager::Assessment
Properties: 
  [AssessmentReportsDestination](#cfn-auditmanager-assessment-assessmentreportsdestination): 
    AssessmentReportsDestination
  [AwsAccount](#cfn-auditmanager-assessment-awsaccount): 
    AWSAccount
  [Delegations](#cfn-auditmanager-assessment-delegations): 
    - Delegation
  [Description](#cfn-auditmanager-assessment-description): String
  [FrameworkId](#cfn-auditmanager-assessment-frameworkid): String
  [Name](#cfn-auditmanager-assessment-name): String
  [Roles](#cfn-auditmanager-assessment-roles): 
    - Role
  [Scope](#cfn-auditmanager-assessment-scope): 
    Scope
  [Status](#cfn-auditmanager-assessment-status): String
  [Tags](#cfn-auditmanager-assessment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-auditmanager-assessment-properties"></a>

`AssessmentReportsDestination`  <a name="cfn-auditmanager-assessment-assessmentreportsdestination"></a>
 The destination that evidence reports are stored in for the assessment\.   
*Required*: No  
*Type*: [AssessmentReportsDestination](aws-properties-auditmanager-assessment-assessmentreportsdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsAccount`  <a name="cfn-auditmanager-assessment-awsaccount"></a>
 The AWS account that's associated with the assessment\.   
*Required*: No  
*Type*: [AWSAccount](aws-properties-auditmanager-assessment-awsaccount.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Delegations`  <a name="cfn-auditmanager-assessment-delegations"></a>
 The delegations that are associated with the assessment\.   
*Required*: No  
*Type*: List of [Delegation](aws-properties-auditmanager-assessment-delegation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-auditmanager-assessment-description"></a>
 The description of the assessment\.   
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Pattern*: `^[\w\W\s\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameworkId`  <a name="cfn-auditmanager-assessment-frameworkid"></a>
The unique identifier for the framework\.  
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `^[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-auditmanager-assessment-name"></a>
 The name of the assessment\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `^[^\\]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Roles`  <a name="cfn-auditmanager-assessment-roles"></a>
 The roles that are associated with the assessment\.   
*Required*: No  
*Type*: List of [Role](aws-properties-auditmanager-assessment-role.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-auditmanager-assessment-scope"></a>
 The wrapper of AWS accounts and services that are in scope for the assessment\.   
*Required*: No  
*Type*: [Scope](aws-properties-auditmanager-assessment-scope.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-auditmanager-assessment-status"></a>
The overall status of the assessment\.  
When you create a new assessment, the initial `Status` value is always `ACTIVE`\. When you create an assessment, even if you specify the value as `INACTIVE`, the value overrides to `ACTIVE`\.   
After you create an assessment, you can change the value of the `Status` property at any time\. For example, when you want to stop collecting evidence for your assessment, you can change the assessment status to `INACTIVE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTIVE | INACTIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-auditmanager-assessment-tags"></a>
 The tags that are associated with the assessment\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
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

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the assessment\. For example, `arn:aws:auditmanager:us-east-1:123456789012:assessment/111A1A1A-22B2-33C3-DDD4-55E5E5E555E5`\. 

`AssessmentId`  <a name="AssessmentId-fn::getatt"></a>
The unique identifier for the assessment\. For example, `111A1A1A-22B2-33C3-DDD4-55E5E5E555E5`\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time when the assessment was created\. For example, `1607582033.373`\.

## See also<a name="aws-resource-auditmanager-assessment--seealso"></a>
+ [CreateAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_CreateAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [DeleteAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_DeleteAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [GetAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_GetAssessment.html) in the *AWS Audit Manager API Reference*\.
+ [UpdateAssessment](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_UpdateAssessment.html) in the *AWS Audit Manager API Reference*\.

