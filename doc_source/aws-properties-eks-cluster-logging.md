# AWS::EKS::Cluster Logging<a name="aws-properties-eks-cluster-logging"></a>

An object representing the logging configuration for resources in your cluster\.

## Syntax<a name="aws-properties-eks-cluster-logging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-cluster-logging-syntax.json"></a>

```
{
  "[ClusterLogging](#cfn-eks-cluster-logging-clusterlogging)" : ClusterLogging
}
```

### YAML<a name="aws-properties-eks-cluster-logging-syntax.yaml"></a>

```
  [ClusterLogging](#cfn-eks-cluster-logging-clusterlogging): 
    ClusterLogging
```

## Properties<a name="aws-properties-eks-cluster-logging-properties"></a>

`ClusterLogging`  <a name="cfn-eks-cluster-logging-clusterlogging"></a>
The cluster control plane logging configuration for your cluster\.  
*Required*: No  
*Type*: [ClusterLogging](aws-properties-eks-cluster-clusterlogging.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)