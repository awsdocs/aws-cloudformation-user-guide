# AWS::SecretsManager::ResourcePolicy<a name="aws-resource-secretsmanager-resourcepolicy"></a>

Attaches the contents of the specified resource\-based permission policy to a secret\. A resource\-based policy is optional\. Alternatively, you can use IAM identity\-based policies that specify the secret's Amazon Resource Name \(ARN\) in the policy statement's `Resources` element\. You can also use a combination of both identity\-based and resource\-based policies\. The affected users and roles receive the permissions that are permitted by all relevant policies\. 

## Syntax<a name="aws-resource-secretsmanager-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::ResourcePolicy",
  "Properties" : {
      "[ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy)" : Json,
      "[SecretId](#cfn-secretsmanager-resourcepolicy-secretid)" : String
    }
}
```

### YAML<a name="aws-resource-secretsmanager-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::SecretsManager::ResourcePolicy
Properties: 
  [ResourcePolicy](#cfn-secretsmanager-resourcepolicy-resourcepolicy): Json
  [SecretId](#cfn-secretsmanager-resourcepolicy-secretid): String
```

## Properties<a name="aws-resource-secretsmanager-resourcepolicy-properties"></a>

`ResourcePolicy`  <a name="cfn-secretsmanager-resourcepolicy-resourcepolicy"></a>
Specifies a JSON object that's constructed according to the grammar and syntax for a resource\-based policy\. The policy identifies who can access or manage this secret and its versions\. For information on how to format a JSON object as a parameter for this resource type, see [Using Resource\-based Policies for Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/UserGuide/auth-and-access-resource-based-policies.html)in the AWS Secrets Manager User Guide\. Those same rules apply here\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretId`  <a name="cfn-secretsmanager-resourcepolicy-secretid"></a>
Specifies the Amazon Resource Name \(ARN\) or the friendly name of the secret that you want to attach a resource\-based permissions policy to\.   
If you use this property to change the `SecretId` for an existing resource\-based policy, it removes the policy from the original secret, and then attaches the policy to the secret with the specified `SecretId`\. This results in changing the permissions for two secrets\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-secretsmanager-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-resourcepolicy-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::ResourcePolicy` resource to the intrinsic `Ref` function, the function returns the ARN of the secret that's being configured, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

This enables you to reference a secret that you create in one part of the stack template from within the definition of another resource later, in the same template\. You would typically use this with the [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) resource type\.

For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-secretsmanager-resourcepolicy--examples"></a>

### Attach a resource\-based policy to a secret<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attach_a_resource-based_policy_to_a_secret"></a>

The following example shows how to attach a resource\-based policy to the specified secret\. The JSON request string input and response output are shown formatted with white space and line breaks for better readability\. Submit your input as a single line JSON string\.

#### JSON<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attach_a_resource-based_policy_to_a_secret--json"></a>

```
 { "MySecret": { "Type": "AWS::SecretsManager::Secret",
            "Properties": { "Description": "This is a secret that I want to attach a resource-based
            policy to" } }, "MySecretResourcePolicy": { "Type":
            "AWS::SecretsManager::ResourcePolicy", "Properties": { "SecretId": {"Ref": "MySecret"},
            "ResourcePolicy": { "Version": "2012-10-17", "Statement": [ { "Effect": "Deny",
            "Principal": {"AWS": {"Fn::Sub": "arn:aws:iam::${AWS::AccountId}:root"}}, "Action":
            "secretsmanager:DeleteSecret", "Resource": "*" } ] } } } }
```

#### YAML<a name="aws-resource-secretsmanager-resourcepolicy--examples--Attach_a_resource-based_policy_to_a_secret--yaml"></a>

```
 MySecret: Type: AWS::SecretsManager::Secret Properties:
            Description: "This is a secret that I want to attach a resource-based policy to" # This
            is a ResourcePolicy resource which attaches a resource policy to the referenced secret.
            # The resource policy denies the DeleteSecret action to all principals in the current
            account. MySecretResourcePolicy: Type: AWS::SecretsManager::ResourcePolicy Properties:
            SecretId: !Ref MySecret ResourcePolicy: Version: "2012-10-17" Statement: - Effect:
            "Deny" Principal: AWS: !Sub "arn:aws:iam::${AWS::AccountId}:root" Action:
            "secretsmanager:DeleteSecret" Resource: "*"
```

## See Also<a name="aws-resource-secretsmanager-resourcepolicy--seealso"></a>
+  [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
