# AWS::SecretsManager::ResourcePolicy<a name="aws-resource-secretsmanager-resourcepolicy"></a>

The `AWS::SecretsManager::ResourcePolicy` resource lets you define a resource\-based policy and attach it to a secret that's stored in Secrets Manager\.

## Syntax<a name="aws-resource-secretsmanager-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::ResourcePolicy",
  "Properties" : {
    "[SecretId](#cfn-secretsmanager-resourcepolicy-secretid)" : String,
    "[ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy)" : JSON object
  }
}
```

### YAML<a name="aws-resource-secretsmanager-resourcepolicy-syntax.yaml"></a>

```
Type: "AWS::SecretsManager::ResourcePolicy"
Properties:
  [SecretId](#cfn-secretsmanager-resourcepolicy-secretid): String
  [ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy): JSON object
```

## Properties<a name="aws-resource-secretsmanager-resourcepolicy-properties"></a>

`SecretId`  <a name="cfn-secretsmanager-resourcepolicy-secretid"></a>
Specifies the Amazon Resource Name \(ARN\) or the friendly name of the secret that you want to attach a resource\-based permissions policy to\. To reference a secret that's also created in this template, use the [Ref](intrinsic-function-reference-ref.md) function with the secret's logical ID\.  
If you use this property to change the `SecretId` for an existing resource\-based policy, it removes the policy from the original secret, and then attaches the policy to the secret with the specified `SecretId`\. This results in changing the permissions for two secrets\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourcePolicy`  <a name="cfn-secretsmanager-resourcepolicy-resourcepolicy"></a>
Specifies a JSON object that's constructed according to the grammar and syntax for an AWSresource\-based policy\. The policy identifies who can access or manage this secret and its versions\. For information on how to format a JSON object as a parameter for this resource type, see [Using Resource\-based Policies for Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_resource-based-policies.html) in the *AWS Secrets Manager User Guide*\. Those same rules apply here\.  
 *Required*: Yes  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-secretsmanager-resourcepolicy-returnvalues"></a>

### Ref<a name="aws-resource-secretsmanager-resourcepolicy-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::ResourcePolicy` resource to the intrinsic `Ref` function, the function returns the ARN of the secret that's being configured, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

This enables you to reference a secret that you create in one part of the stack template from within the definition of another resource later, in the same template\. You would typically use this with the [AWS::SecretsManager::SecretTargetAttachment](aws-resource-secretsmanager-secrettargetattachment.md) resource type\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-secretsmanager-resourcepolicy-examples"></a>

### Attaching a Resource\-based Policy to a Secret<a name="aws-resource-secretsmanager-resourcepolicy-example1"></a>

The following example shows how to define a resource\-based policy and attach it to a secret that you previously defined\. It defines a secret with the logical name `MySecretForAppA`, and then attaches a resource\-based permissions policy to it\.

**Note**  
The JSON specification doesn't allow any kind of comments\. See the YAML example for comments\.

#### JSON<a name="aws-resource-secretsmanager-resourcepolicy-example1.json"></a>

```
{
  "MySecret": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Description": "This is a secret that I want to attach a resource-based policy to"
    }
  },
  "MySecretResourcePolicy": {
    "Type": "AWS::SecretsManager::ResourcePolicy",
    "Properties": {
      "SecretId": {"Ref": "MySecret"},
      "ResourcePolicy": {
        "Version": "2012-10-17",
        "Statement": [
          {
            "Effect": "Deny",
            "Principal": {"AWS": {"Fn::Sub": "arn:aws:iam::${AWS::AccountId}:root"}},
            "Action": "secretsmanager:DeleteSecret",
            "Resource": "*"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-resourcepolicy-example1.yaml"></a>

```
MySecret:
  Type: AWS::SecretsManager::Secret
  Properties:
    Description: "This is a secret that I want to attach a resource-based policy to"

# This is a ResourcePolicy resource which attaches a resource policy to the referenced secret.
# The resource policy denies the DeleteSecret action to all principals in the current account.
MySecretResourcePolicy:
  Type: AWS::SecretsManager::ResourcePolicy
  Properties:
    SecretId: !Ref MySecret
    ResourcePolicy:
      Version: "2012-10-17"
      Statement:
        -
          Effect: "Deny"
          Principal:
            AWS: !Sub "arn:aws:iam::${AWS::AccountId}:root"
          Action: "secretsmanager:DeleteSecret"
          Resource: "*"
```

## See Also<a name="aws-resource-secretsmanager-resourcepolicy-seealso"></a>
+ For information about using resource\-based policies with Secrets Manager, see [Using Resource\-based Policies for Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_resource-based-policies.html) in the *AWS Secrets Manager User Guide*\. 
+ [AWS::SecretsManager::Secret](aws-resource-secretsmanager-secret.md)
+ [AWS::SecretsManager::SecretTargetAttachment](aws-resource-secretsmanager-secrettargetattachment.md)
+ [AWS::SecretsManager::RotationSchedule](aws-resource-secretsmanager-rotationschedule.md)