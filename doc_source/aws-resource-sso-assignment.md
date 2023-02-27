# AWS::SSO::Assignment<a name="aws-resource-sso-assignment"></a>

Assigns access to a Principal for a specified AWS account using a specified permission set\.

**Note**  
The term *principal* here refers to a user or group that is defined in IAM Identity Center\.

## Syntax<a name="aws-resource-sso-assignment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sso-assignment-syntax.json"></a>

```
{
  "Type" : "AWS::SSO::Assignment",
  "Properties" : {
      "[InstanceArn](#cfn-sso-assignment-instancearn)" : String,
      "[PermissionSetArn](#cfn-sso-assignment-permissionsetarn)" : String,
      "[PrincipalId](#cfn-sso-assignment-principalid)" : String,
      "[PrincipalType](#cfn-sso-assignment-principaltype)" : String,
      "[TargetId](#cfn-sso-assignment-targetid)" : String,
      "[TargetType](#cfn-sso-assignment-targettype)" : String
    }
}
```

### YAML<a name="aws-resource-sso-assignment-syntax.yaml"></a>

```
Type: AWS::SSO::Assignment
Properties: 
  [InstanceArn](#cfn-sso-assignment-instancearn): String
  [PermissionSetArn](#cfn-sso-assignment-permissionsetarn): String
  [PrincipalId](#cfn-sso-assignment-principalid): String
  [PrincipalType](#cfn-sso-assignment-principaltype): String
  [TargetId](#cfn-sso-assignment-targetid): String
  [TargetType](#cfn-sso-assignment-targettype): String
```

## Properties<a name="aws-resource-sso-assignment-properties"></a>

`InstanceArn`  <a name="cfn-sso-assignment-instancearn"></a>
The ARN of the IAM Identity Center instance under which the operation will be executed\. For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):sso:::instance/(sso)?ins-[a-zA-Z0-9-.]{16}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionSetArn`  <a name="cfn-sso-assignment-permissionsetarn"></a>
The ARN of the permission set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):sso:::permissionSet/(sso)?ins-[a-zA-Z0-9-.]{16}/ps-[a-zA-Z0-9-./]{16}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalId`  <a name="cfn-sso-assignment-principalid"></a>
An identifier for an object in IAM Identity Center, such as a user or group\. PrincipalIds are GUIDs \(For example, f81d4fae\-7dec\-11d0\-a765\-00a0c91e6bf6\)\. For more information about PrincipalIds in IAM Identity Center, see the [IAM Identity Center Identity Store API Reference](/singlesignon/latest/IdentityStoreAPIReference/welcome.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `47`  
*Pattern*: `^([0-9a-f]{10}-|)[A-Fa-f0-9]{8}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalType`  <a name="cfn-sso-assignment-principaltype"></a>
The entity type for which the assignment will be created\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GROUP | USER`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetId`  <a name="cfn-sso-assignment-targetid"></a>
TargetID is an AWS account identifier, typically a 10\-12 digit string \(For example, 123456789012\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `\d{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetType`  <a name="cfn-sso-assignment-targettype"></a>
The entity type for which the assignment will be created\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AWS_ACCOUNT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sso-assignment-return-values"></a>

### Ref<a name="aws-resource-sso-assignment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a generated ID, combined by all fields with the delimiter `|`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-sso-assignment--examples"></a>



### Creating a new assignment for IAM Identity Center<a name="aws-resource-sso-assignment--examples--Creating_a_new_assignment_for_"></a>

The following example creates a custom assignment, assigning the user `"user_id"` access to account `"arn:aws:organizations::org_master_id:account/org_id/accountId"` with the permissions `"PermissionSet"`\. 

#### JSON<a name="aws-resource-sso-assignment--examples--Creating_a_new_assignment_for_--json"></a>

```
{
   "Assignment": {
      "Type": "AWS::SSO::Assignment",
      "Properties": {
         "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
         "PermissionSetArn": {
            "Fn::GetAtt": [
               "PermissionSet",
               "PermissionSetArn"
            ]
         },
         "TargetId": "accountId",
         "TargetType": "AWS_ACCOUNT",
         "PrincipalType": "USER",
         "PrincipalId": "user_id"
      }
   }
}
```

#### YAML<a name="aws-resource-sso-assignment--examples--Creating_a_new_assignment_for_--yaml"></a>

```
Assignment:
    Type: AWS::SSO::Assignment
    Properties:
      InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
      PermissionSetArn: !GetAtt PermissionSet.PermissionSetArn
      TargetId: 'accountId'
      TargetType: 'AWS_ACCOUNT'
      PrincipalType: 'USER'
      PrincipalId: 'user_id'
```