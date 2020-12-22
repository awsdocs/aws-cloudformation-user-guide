# AWS::AuditManager::Assessment AWSAccount<a name="aws-properties-auditmanager-assessment-awsaccount"></a>

 The `AWSAccount` property type specifies the wrapper of the AWS account details, such as account ID, email address, and so on\. 

## Syntax<a name="aws-properties-auditmanager-assessment-awsaccount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-auditmanager-assessment-awsaccount-syntax.json"></a>

```
{
  "[emailAddress](#cfn-auditmanager-assessment-awsaccount-emailaddress)" : String,
  "[id](#cfn-auditmanager-assessment-awsaccount-id)" : String,
  "[name](#cfn-auditmanager-assessment-awsaccount-name)" : String
}
```

### YAML<a name="aws-properties-auditmanager-assessment-awsaccount-syntax.yaml"></a>

```
  [emailAddress](#cfn-auditmanager-assessment-awsaccount-emailaddress): String
  [id](#cfn-auditmanager-assessment-awsaccount-id): String
  [name](#cfn-auditmanager-assessment-awsaccount-name): String
```

## Properties<a name="aws-properties-auditmanager-assessment-awsaccount-properties"></a>

`emailAddress`  <a name="cfn-auditmanager-assessment-awsaccount-emailaddress"></a>
 The email address associated with the specified AWS account\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `320`  
*Pattern*: `^.*@.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`id`  <a name="cfn-auditmanager-assessment-awsaccount-id"></a>
 The identifier for the specified AWS account\.   
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`name`  <a name="cfn-auditmanager-assessment-awsaccount-name"></a>
 The name of the specified AWS account\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `^[\u0020-\u007E]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-auditmanager-assessment-awsaccount--seealso"></a>
+ [AWSAccount](https://docs.aws.amazon.com/audit-manager/latest/APIReference/API_AWSAccount.html) in the *AWS Audit Manager API Reference*\.

