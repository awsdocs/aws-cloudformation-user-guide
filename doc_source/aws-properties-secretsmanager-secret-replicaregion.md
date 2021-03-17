# AWS::SecretsManager::Secret ReplicaRegion<a name="aws-properties-secretsmanager-secret-replicaregion"></a>

The `AWS::SecretsManager::Secret` property used to enable cross\-region replication\. For more details see [Multi\-Region Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/create-manage-multi-region-secrets.html)\.

## Syntax<a name="aws-properties-secretsmanager-secret-replicaregion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-secret-replicaregion-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-secretsmanager-secret-replicaregion-kmskeyid)" : String,
  "[Region](#cfn-secretsmanager-secret-replicaregion-region)" : String
}
```

### YAML<a name="aws-properties-secretsmanager-secret-replicaregion-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-secretsmanager-secret-replicaregion-kmskeyid): String
  [Region](#cfn-secretsmanager-secret-replicaregion-region): String
```

## Properties<a name="aws-properties-secretsmanager-secret-replicaregion-properties"></a>

`KmsKeyId`  <a name="cfn-secretsmanager-secret-replicaregion-kmskeyid"></a>
\(Optional\) Specifies the ARN, Key ID, or alias of the AWS KMS customer master key \(CMK\) used to encrypt the `SecretString` or `SecretBinary` values for versions of this secret\. If you don't specify this value, then Secrets Manager defaults to the AWS account CMK, `aws/secretsmanager`\. If an AWS KMS CMK with that name doesn't exist, Secrets Manager creates the CMK for you automatically the first time it encrypts a version `SecretString` or `SecretBinary` fields\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-secretsmanager-secret-replicaregion-region"></a>
Specifies the region location of the replica secret\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)