# AWS::EKS::Nodegroup Taint<a name="aws-properties-eks-nodegroup-taint"></a>

A property that allows a node to repel a set of pods\. For more information, see [Node taints on managed node groups](https://docs.aws.amazon.com/eks/latest/userguide/node-taints-managed-node-groups.html)\.

## Syntax<a name="aws-properties-eks-nodegroup-taint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-nodegroup-taint-syntax.json"></a>

```
{
  "[Effect](#cfn-eks-nodegroup-taint-effect)" : String,
  "[Key](#cfn-eks-nodegroup-taint-key)" : String,
  "[Value](#cfn-eks-nodegroup-taint-value)" : String
}
```

### YAML<a name="aws-properties-eks-nodegroup-taint-syntax.yaml"></a>

```
  [Effect](#cfn-eks-nodegroup-taint-effect): String
  [Key](#cfn-eks-nodegroup-taint-key): String
  [Value](#cfn-eks-nodegroup-taint-value): String
```

## Properties<a name="aws-properties-eks-nodegroup-taint-properties"></a>

`Effect`  <a name="cfn-eks-nodegroup-taint-effect"></a>
The effect of the taint\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NO_EXECUTE | NO_SCHEDULE | PREFER_NO_SCHEDULE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-eks-nodegroup-taint-key"></a>
The key of the taint\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-eks-nodegroup-taint-value"></a>
The value of the taint\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `63`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)