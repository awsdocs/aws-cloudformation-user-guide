# AWS::MSK::Cluster Unauthenticated<a name="aws-properties-msk-cluster-unauthenticated"></a>

Details for allowing no client authentication\.

## Syntax<a name="aws-properties-msk-cluster-unauthenticated-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-unauthenticated-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-cluster-unauthenticated-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-unauthenticated-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-cluster-unauthenticated-enabled): Boolean
```

## Properties<a name="aws-properties-msk-cluster-unauthenticated-properties"></a>

`Enabled`  <a name="cfn-msk-cluster-unauthenticated-enabled"></a>
Unauthenticated is enabled or not\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)