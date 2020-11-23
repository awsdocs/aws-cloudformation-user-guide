# AWS::EKS::FargateProfile Selector<a name="aws-properties-eks-fargateprofile-selector"></a>

An object representing an AWS Fargate profile selector\.

## Syntax<a name="aws-properties-eks-fargateprofile-selector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-fargateprofile-selector-syntax.json"></a>

```
{
  "[Labels](#cfn-eks-fargateprofile-selector-labels)" : [ Label, ... ],
  "[Namespace](#cfn-eks-fargateprofile-selector-namespace)" : String
}
```

### YAML<a name="aws-properties-eks-fargateprofile-selector-syntax.yaml"></a>

```
  [Labels](#cfn-eks-fargateprofile-selector-labels): 
    - Label
  [Namespace](#cfn-eks-fargateprofile-selector-namespace): String
```

## Properties<a name="aws-properties-eks-fargateprofile-selector-properties"></a>

`Labels`  <a name="cfn-eks-fargateprofile-selector-labels"></a>
The Kubernetes labels that the selector should match\. A pod must contain all of the labels that are specified in the selector for it to be considered a match\.  
*Required*: No  
*Type*: List of [Label](aws-properties-eks-fargateprofile-label.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Namespace`  <a name="cfn-eks-fargateprofile-selector-namespace"></a>
The Kubernetes namespace that the selector should match\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)