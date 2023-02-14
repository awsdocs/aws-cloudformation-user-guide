# AWS::EKS::Cluster Logging<a name="aws-properties-eks-cluster-logging"></a>

Enable or disable exporting the Kubernetes control plane logs for your cluster to CloudWatch Logs\. By default, cluster control plane logs aren't exported to CloudWatch Logs\. For more information, see [Amazon EKS Cluster control plane logs](https://docs.aws.amazon.com/eks/latest/userguide/control-plane-logs.html) in the * *Amazon EKS User Guide* *\.

**Important**  
When updating a resource, you must include this `Logging` property if the previous CloudFormation template of the resource had it\.

**Note**  
CloudWatch Logs ingestion, archive storage, and data scanning rates apply to exported control plane logs\. For more information, see [CloudWatch Pricing](http://aws.amazon.com/cloudwatch/pricing/)\.

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