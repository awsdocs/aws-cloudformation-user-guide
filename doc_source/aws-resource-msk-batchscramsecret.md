# AWS::MSK::BatchScramSecret<a name="aws-resource-msk-batchscramsecret"></a>

Represents a secret stored in the Amazon Secrets Manager that can be used to authenticate with a cluster using your sign\-in credentials\.

## Syntax<a name="aws-resource-msk-batchscramsecret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-batchscramsecret-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::BatchScramSecret",
  "Properties" : {
      "[ClusterArn](#cfn-msk-batchscramsecret-clusterarn)" : String,
      "[SecretArnList](#cfn-msk-batchscramsecret-secretarnlist)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-msk-batchscramsecret-syntax.yaml"></a>

```
Type: AWS::MSK::BatchScramSecret
Properties: 
  [ClusterArn](#cfn-msk-batchscramsecret-clusterarn): String
  [SecretArnList](#cfn-msk-batchscramsecret-secretarnlist): 
    - String
```

## Properties<a name="aws-resource-msk-batchscramsecret-properties"></a>

`ClusterArn`  <a name="cfn-msk-batchscramsecret-clusterarn"></a>
The Amazon Resource Name \(ARN\) of the MSK cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecretArnList`  <a name="cfn-msk-batchscramsecret-secretarnlist"></a>
A list of Amazon Secrets Manager secret ARNs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-msk-batchscramsecret-return-values"></a>

### Ref<a name="aws-resource-msk-batchscramsecret-return-values-ref"></a>

The ARN of the cluster\.