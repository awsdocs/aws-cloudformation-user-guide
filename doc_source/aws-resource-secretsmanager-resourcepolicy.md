# AWS::SecretsManager::ResourcePolicy<a name="aws-resource-secretsmanager-resourcepolicy"></a>

Attaches the contents of the specified resource\-based permission policy to a secret\. A resource\-based policy is optional\. Alternatively, you can use IAM identity\-based policies to specify the Amazon Resource Name \(ARN\) of the secret in the policy statement `Resources` element\. You can also use a combination of both identity\-based and resource\-based policies\. The affected users and roles receive the permissions permitted by all relevant policies\. 

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
Specifies if you configuired a check for a resource policy that exposes information publicly\.  
For more information on using this parameter, see [Managing a resource\-based policy for a secret](https://docs.aws.amazon.com/secretsmanager/latest/userguide/manage_secret-policy.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcePolicy`  <a name="cfn-secretsmanager-resourcepolicy-resourcepolicy"></a>
Specifies a JSON object constructed according to the grammar and syntax for a resource\-based policy\. The policy identifies who can access or manage this secret and associated versions\. For information on how to format a JSON object as a parameter for this resource type, see [Using Resource\-based Policies for Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/auth-and-access_resource-based-policies.html) in the AWS Secrets Manager User Guide\. Those same rules apply here\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-resourcepolicy-secretid"></a>
Specifies the Amazon Resource Name \(ARN\) or the friendly name of the secret to attach a resource\-based permissions policy\.   
If you use this property to change the `SecretId` for an existing resource\-based policy, Secrets Manager removes the policy from the original secret, and then attaches the policy to the secret with the specified `SecretId`\. This results in changing the permissions for two secrets\.
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

### Attaching a resource\-based policy to an RDS DB Instance secret<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_DB_Instance_secret_"></a>

The following examples shows how to attach a resource\-based policy to the specified secret\. The JSON request string input and response output displays as formatted with white space and line breaks for better readability\. Submit your input as a single line JSON string\.

#### JSON<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_DB_Instance_secret_--json"></a>

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
            "BlockPublicPolicy": {
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
}
```

#### YAML<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attaching_a_resource-based_policy_to_an_RDS_DB_Instance_secret_--yaml"></a>

```
MySecret:
    Type: 'AWS::SecretsManager::Secret'
    Properties:
        Description: This is a secret that I want to attach a resource-based policy to
MySecretResourcePolicy:
    Type: 'AWS::SecretsManager::ResourcePolicy'
    Properties:
        SecretId: !Ref MySecret
        ResourcePolicy:
          Version: 2012-10-17
          Statement:
            - Resource: '*'
              Action: 'secretsmanager:DeleteSecret'
              Effect: Deny
              Principal:
                AWS: !Sub 'arn:aws:iam::${AWS::AccountId}:root'
```

## See also<a name="aws-resource-secretsmanager-resourcepolicy--seealso"></a>
+  [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)