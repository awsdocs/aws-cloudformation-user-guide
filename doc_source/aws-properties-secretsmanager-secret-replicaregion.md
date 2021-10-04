# AWS::SecretsManager::Secret ReplicaRegion<a name="aws-properties-secretsmanager-secret-replicaregion"></a>

\(Optional\) Custom type consisting of a `Region` \(required\) and the `KmsKeyId` which can be an `ARN`, `Key ID`, or `Alias`\.

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
Can be an `ARN`, `Key ID`, or `Alias`\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-secretsmanager-secret-replicaregion-region"></a>
\(Optional\) A string that represents a `Region`, for example "us\-east\-1"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)