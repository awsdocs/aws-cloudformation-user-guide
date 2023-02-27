# AWS::ECS::Service Secret<a name="aws-properties-ecs-service-secret"></a>

An object representing the secret to expose to your container\. Secrets can be exposed to a container in the following ways:
+ To inject sensitive data into your containers as environment variables, use the `secrets` container definition parameter\.
+ To reference sensitive information in the log configuration of a container, use the `secretOptions` container definition parameter\.

For more information, see [Specifying sensitive data](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/specifying-sensitive-data.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-secret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-secret-syntax.json"></a>

```
{
  "[Name](#cfn-ecs-service-secret-name)" : String,
  "[ValueFrom](#cfn-ecs-service-secret-valuefrom)" : String
}
```

### YAML<a name="aws-properties-ecs-service-secret-syntax.yaml"></a>

```
  [Name](#cfn-ecs-service-secret-name): String
  [ValueFrom](#cfn-ecs-service-secret-valuefrom): String
```

## Properties<a name="aws-properties-ecs-service-secret-properties"></a>

`Name`  <a name="cfn-ecs-service-secret-name"></a>
The name of the secret\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueFrom`  <a name="cfn-ecs-service-secret-valuefrom"></a>
The secret to expose to the container\. The supported values are either the full ARN of the AWS Secrets Manager secret or the full ARN of the parameter in the SSM Parameter Store\.  
For information about the require AWS Identity and Access Management permissions, see [Required IAM permissions for Amazon ECS secrets](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/specifying-sensitive-data-secrets.html#secrets-iam) \(for Secrets Manager\) or [Required IAM permissions for Amazon ECS secrets](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/specifying-sensitive-data-parameters.html) \(for Systems Manager Parameter store\) in the *Amazon Elastic Container Service Developer Guide*\.  
If the SSM Parameter Store parameter exists in the same Region as the task you're launching, then you can use either the full ARN or name of the parameter\. If the parameter exists in a different Region, then the full ARN must be specified\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)