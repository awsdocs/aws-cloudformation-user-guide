# DynamoDB Accelerator Cluster SSESpecification<a name="aws-properties-daxservice-cluster-ssespecification"></a>

<a name="aws-properties-daxservice-cluster-ssespecification-description"></a>The `SSESpecification` property type specifies whether server\-side encryption is enabled or not\.

If you do not specify the `SSESpecification` property type, DAX will create an unencrypted cluster, the same as if you had specified the `SSESpecification` property type with its `SSEEnabled` property set to `false`\. 

<a name="aws-properties-daxservice-cluster-ssespecification-inheritance"></a> `SSESpecification` is a property of the [AWS::DAX::Cluster](aws-resource-dax-cluster.md) resource\.

## Syntax<a name="aws-properties-daxservice-cluster-ssespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-daxservice-cluster-ssespecification-syntax.json"></a>

```
{
  "[SSEEnabled](#cfn-daxservice-cluster-ssespecification-sseenabled)" : Boolean
}
```

### YAML<a name="aws-properties-daxservice-cluster-ssespecification-syntax.yaml"></a>

```
[SSEEnabled](#cfn-daxservice-cluster-ssespecification-sseenabled): Boolean
```

## Properties<a name="aws-properties-daxservice-cluster-ssespecification-properties"></a>

`SSEEnabled`  <a name="cfn-daxservice-cluster-ssespecification-sseenabled"></a>
Whether server\-side encryption is enabled or not\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-daxservice-cluster-ssespecification-seealso"></a>
+ [SSESpecification](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_SSESpecification.html) in the *Amazon DynamoDB API Reference*