# AWS::DAX::Cluster SSESpecification<a name="aws-properties-dax-cluster-ssespecification"></a>

Represents the settings used to enable server\-side encryption\.

## Syntax<a name="aws-properties-dax-cluster-ssespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dax-cluster-ssespecification-syntax.json"></a>

```
{
  "[SSEEnabled](#cfn-dax-cluster-ssespecification-sseenabled)" : Boolean
}
```

### YAML<a name="aws-properties-dax-cluster-ssespecification-syntax.yaml"></a>

```
  [SSEEnabled](#cfn-dax-cluster-ssespecification-sseenabled): Boolean
```

## Properties<a name="aws-properties-dax-cluster-ssespecification-properties"></a>

`SSEEnabled`  <a name="cfn-dax-cluster-ssespecification-sseenabled"></a>
Indicates whether server\-side encryption is enabled \(true\) or disabled \(false\) on the cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)