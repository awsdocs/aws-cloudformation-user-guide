# AWS::ECR::PullThroughCacheRule<a name="aws-resource-ecr-pullthroughcacherule"></a>

Creates a pull through cache rule\. A pull through cache rule provides a way to cache images from an external public registry in your Amazon ECR private registry\.

## Syntax<a name="aws-resource-ecr-pullthroughcacherule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-pullthroughcacherule-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::PullThroughCacheRule",
  "Properties" : {
      "[EcrRepositoryPrefix](#cfn-ecr-pullthroughcacherule-ecrrepositoryprefix)" : String,
      "[UpstreamRegistryUrl](#cfn-ecr-pullthroughcacherule-upstreamregistryurl)" : String
    }
}
```

### YAML<a name="aws-resource-ecr-pullthroughcacherule-syntax.yaml"></a>

```
Type: AWS::ECR::PullThroughCacheRule
Properties: 
  [EcrRepositoryPrefix](#cfn-ecr-pullthroughcacherule-ecrrepositoryprefix): String
  [UpstreamRegistryUrl](#cfn-ecr-pullthroughcacherule-upstreamregistryurl): String
```

## Properties<a name="aws-resource-ecr-pullthroughcacherule-properties"></a>

`EcrRepositoryPrefix`  <a name="cfn-ecr-pullthroughcacherule-ecrrepositoryprefix"></a>
The Amazon ECR repository prefix associated with the pull through cache rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `20`  
*Pattern*: `[a-z0-9]+(?:[._-][a-z0-9]+)*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UpstreamRegistryUrl`  <a name="cfn-ecr-pullthroughcacherule-upstreamregistryurl"></a>
The upstream registry URL associated with the pull through cache rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-ecr-pullthroughcacherule--examples"></a>

The following resource examples show how to create a pull through cache rule for a private registry\.

### Create a pull through cache rule for a private registry<a name="aws-resource-ecr-pullthroughcacherule--examples--Create_a_pull_through_cache_rule_for_a_private_registry"></a>

The following example creates a pull through cache rule that caches repositories with the name prefix `my-ecr` from the Amazon ECR Public registry into your private registry\.

#### JSON<a name="aws-resource-ecr-pullthroughcacherule--examples--Create_a_pull_through_cache_rule_for_a_private_registry--json"></a>

```
{
    "Resources": {
        "MyECRPullThroughCacheRule": {
            "Type": "AWS::ECR::PullThroughCacheRule",
            "Properties": {
                "EcrRepositoryPrefix": "my-ecr",
                "UpstreamRegistryUrl": "public.ecr.aws"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecr-pullthroughcacherule--examples--Create_a_pull_through_cache_rule_for_a_private_registry--yaml"></a>

```
Resources:
  MyECRPullThroughCacheRule:
    Type: 'AWS::ECR::PullThroughCacheRule'
    Properties:
      EcrRepositoryPrefix: 'my-ecr'
      UpstreamRegistryUrl: 'public.ecr.aws'
```