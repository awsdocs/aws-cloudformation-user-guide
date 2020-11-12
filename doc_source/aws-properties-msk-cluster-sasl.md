# AWS::MSK::Cluster Sasl<a name="aws-properties-msk-cluster-sasl"></a>

Details for client authentication using SASL\.

## Syntax<a name="aws-properties-msk-cluster-sasl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-sasl-syntax.json"></a>

```
{
  "[Scram](#cfn-msk-cluster-sasl-scram)" : Scram
}
```

### YAML<a name="aws-properties-msk-cluster-sasl-syntax.yaml"></a>

```
  [Scram](#cfn-msk-cluster-sasl-scram): 
    Scram
```

## Properties<a name="aws-properties-msk-cluster-sasl-properties"></a>

`Scram`  <a name="cfn-msk-cluster-sasl-scram"></a>
Details for SASL/SCRAM client authentication\.  
*Required*: Yes  
*Type*: [Scram](aws-properties-msk-cluster-scram.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)