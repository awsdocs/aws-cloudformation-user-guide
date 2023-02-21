# AWS::SecretsManager::ResourcePolicy<a name="aws-resource-secretsmanager-resourcepolicy"></a>

Attaches a resource\-based permission policy to a secret\. A resource\-based policy is optional\. For more information, see [Authentication and access control for Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access.html) 

For information about attaching a policy in the console, see [Attach a permissions policy to a secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_resource-based-policies.html)\.

 **Required permissions: ** `secretsmanager:PutResourcePolicy`\. For more information, see [ IAM policy actions for Secrets Manager](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awssecretsmanager.html#awssecretsmanager-actions-as-permissions) and [Authentication and access control in Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access.html)\. 

## Syntax<a name="aws-resource-secretsmanager-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::ResourcePolicy",
  "Properties" : {
      "[BlockPublicPolicy](#cfn-secretsmanager-resourcepolicy-blockpublicpolicy)" : Boolean,
      "[ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy)" : Json,
      "[SecretId](#cfn-secretsmanager-resourcepolicy-secretid)" : String
    }
}
```

### YAML<a name="aws-resource-secretsmanager-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::SecretsManager::ResourcePolicy
Properties: 
  [BlockPublicPolicy](#cfn-secretsmanager-resourcepolicy-blockpublicpolicy): Boolean
  [ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy): Json
  [SecretId](#cfn-secretsmanager-resourcepolicy-secretid): String
```

## Properties<a name="aws-resource-secretsmanager-resourcepolicy-properties"></a>

`BlockPublicPolicy`  <a name="cfn-secretsmanager-resourcepolicy-blockpublicpolicy"></a>
Specifies whether to block resource\-based policies that allow broad access to the secret\. By default, Secrets Manager blocks policies that allow broad access, for example those that use a wildcard for the principal\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcePolicy`  <a name="cfn-secretsmanager-resourcepolicy-resourcepolicy"></a>
A JSON\-formatted string for an AWS resource\-based policy\. For example policies, see [Permissions policy examples](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_examples.html)\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-resourcepolicy-secretid"></a>
The ARN or name of the secret to attach the resource\-based policy\.  
For an ARN, we recommend that you specify a complete ARN rather than a partial ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-secretsmanager-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-resourcepolicy-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::ResourcePolicy` resource to the intrinsic `Ref` function, the function returns the ARN of the configured secret, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

This enables you to reference a secret you created in one part of the stack template from within the definition of another resource later, in the same template\. You would typically use this with the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the Ref function, see [Ref](url-doc-domain/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-secretsmanager-resourcepolicy--examples"></a>

### Attaching a resource\-based policy to an RDS database instance secret<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_database_instance_secret_"></a>

The following example shows how to attach a resource\-based policy to a secret\. The JSON request string input and response output displays as formatted with white space and line breaks for better readability\. Submit your input as a single line JSON string\.

#### JSON<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_database_instance_secret_--json"></a>

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
      "BlockPublicPolicy": "True",
      "SecretId": {
        "Ref": "MySecret"
      },
      "ResourcePolicy": {
        "Version": "2012-10-17",
        "Statement": [
        {
          "Resource": "*",
          "Action": "secretsmanager:DeleteSecret",
          "Effect": "Deny",
          "Principal": {
            "AWS": {
              "Fn::Sub": "arn:aws:iam::${AWS::AccountId}:root"
            }
          }
        }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_database_instance_secret_--yaml"></a>

```
---
MySecret:
  Type: AWS::SecretsManager::Secret
  Properties:
        Description: This is a secret that I want to attach a resource-based policy to
MySecretResourcePolicy:
  Type: AWS::SecretsManager::ResourcePolicy
  Properties:
    BlockPublicPolicy: True
    SecretId:
      Ref: MySecret
    ResourcePolicy:
      Version: '2012-10-17'
      Statement:
      - Resource: "*"
        Action: secretsmanager:DeleteSecret
        Effect: Deny
        Principal:
          AWS:
            Fn::Sub: arn:aws:iam::${AWS::AccountId}:root
```

## See also<a name="aws-resource-secretsmanager-resourcepolicy--seealso"></a>
+  [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)