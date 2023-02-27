# AWS::SecretsManager::Secret ReplicaRegion<a name="aws-properties-secretsmanager-secret-replicaregion"></a>

Specifies a `Region` and the `KmsKeyId` for a replica secret\.

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
The ARN, key ID, or alias of the KMS key to encrypt the secret\. If you don't include this field, Secrets Manager uses `aws/secretsmanager`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-secretsmanager-secret-replicaregion-region"></a>
\(Optional\) A string that represents a `Region`, for example "us\-east\-1"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)