# AWS::ECR::Repository LifecyclePolicy<a name="aws-properties-ecr-repository-lifecyclepolicy"></a>

The `LifecyclePolicy` property type specifies a lifecycle policy\. For information about lifecycle policy syntax, see [Lifecycle Policy Template](https://docs.aws.amazon.com/AmazonECR/latest/userguide/LifecyclePolicies.html)\.

## Syntax<a name="aws-properties-ecr-repository-lifecyclepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-repository-lifecyclepolicy-syntax.json"></a>

```
{
  "[LifecyclePolicyText](#cfn-ecr-repository-lifecyclepolicy-lifecyclepolicytext)" : String,
  "[RegistryId](#cfn-ecr-repository-lifecyclepolicy-registryid)" : String
}
```

### YAML<a name="aws-properties-ecr-repository-lifecyclepolicy-syntax.yaml"></a>

```
  [LifecyclePolicyText](#cfn-ecr-repository-lifecyclepolicy-lifecyclepolicytext): String
  [RegistryId](#cfn-ecr-repository-lifecyclepolicy-registryid): String
```

## Properties<a name="aws-properties-ecr-repository-lifecyclepolicy-properties"></a>

`LifecyclePolicyText`  <a name="cfn-ecr-repository-lifecyclepolicy-lifecyclepolicytext"></a>
The JSON repository policy text to apply to the repository\.  
*Required*: No  
*Type*: String  
*Minimum*: `100`  
*Maximum*: `30720`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryId`  <a name="cfn-ecr-repository-lifecyclepolicy-registryid"></a>
The AWS account ID associated with the registry that contains the repository\. If you do  not specify a registry, the default registry is assumed\.  
*Required*: No  
*Type*: String  
*Pattern*: `[0-9]{12}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ecr-repository-lifecyclepolicy--seealso"></a>
+  [Creating a Lifecycle Policy](https://docs.aws.amazon.com/AmazonECR/latest/userguide/lp_creation.html) in the *Amazon Elastic Container Registry User Guide* 
+  [PutLifecyclePolicy](https://docs.aws.amazon.com/AmazonECR/latest/APIReference/API_PutLifecyclePolicy.html) in the *Amazon Elastic Container Registry API Reference* 

## Supported Regions

This PropertyType is supported by ***all*** regions.