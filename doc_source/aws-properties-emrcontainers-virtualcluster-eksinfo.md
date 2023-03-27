# AWS::EMRContainers::VirtualCluster EksInfo<a name="aws-properties-emrcontainers-virtualcluster-eksinfo"></a>

The information about the Amazon EKS cluster\.

## Syntax<a name="aws-properties-emrcontainers-virtualcluster-eksinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrcontainers-virtualcluster-eksinfo-syntax.json"></a>

```
{
  "[Namespace](#cfn-emrcontainers-virtualcluster-eksinfo-namespace)" : String
}
```

### YAML<a name="aws-properties-emrcontainers-virtualcluster-eksinfo-syntax.yaml"></a>

```
  [Namespace](#cfn-emrcontainers-virtualcluster-eksinfo-namespace): String
```

## Properties<a name="aws-properties-emrcontainers-virtualcluster-eksinfo-properties"></a>

`Namespace`  <a name="cfn-emrcontainers-virtualcluster-eksinfo-namespace"></a>
The namespaces of the EKS cluster\.  
*Minimum*: 1  
*Maximum*: 63  
*Pattern*: `[a-z0-9]([-a-z0-9]*[a-z0-9])?`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)