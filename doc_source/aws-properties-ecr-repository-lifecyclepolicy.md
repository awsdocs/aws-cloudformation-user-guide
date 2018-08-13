# Amazon Elastic Container Registry Repository LifecyclePolicy<a name="aws-properties-ecr-repository-lifecyclepolicy"></a>

<a name="aws-properties-ecr-repository-lifecyclepolicy-description"></a>The `LifecyclePolicy` property type specifies a lifecycle policy for an Amazon Elastic Container Registry \(Amazon ECR\) repository\.

<a name="aws-properties-ecr-repository-lifecyclepolicy-inheritance"></a> `LifecyclePolicy` is a property of the [AWS::ECR::Repository](aws-resource-ecr-repository.md) resource\.

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
The JSON repository policy text to apply to the repository\. The length must be between 100 and 10,240 characters\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RegistryId`  <a name="cfn-ecr-repository-lifecyclepolicy-registryid"></a>
The AWS account ID that's associated with the registry that contains the repository\. If you do n't specify a registry, the default registry is used\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ecr-repository-lifecyclepolicy-seealso"></a>
+ [ Creating a Lifecycle Policy](http://docs.aws.amazon.com/AmazonECR/latest/userguide/lp_creation.html) in the *Amazon Elastic Container Registry User Guide*
+ [ PutLifecyclePolicy](http://docs.aws.amazon.com/AmazonECR/latest/APIReference/API_PutLifecyclePolicy.html) in the *Amazon Elastic Container Registry API Reference*