# AWS::Batch::JobDefinition PodProperties<a name="aws-properties-batch-jobdefinition-podproperties"></a>

The properties for the pod\.

## Syntax<a name="aws-properties-batch-jobdefinition-podproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-podproperties-syntax.json"></a>

```
{
  "[Containers](#cfn-batch-jobdefinition-podproperties-containers)" : [ EksContainer, ... ],
  "[DnsPolicy](#cfn-batch-jobdefinition-podproperties-dnspolicy)" : String,
  "[HostNetwork](#cfn-batch-jobdefinition-podproperties-hostnetwork)" : Boolean,
  "[ServiceAccountName](#cfn-batch-jobdefinition-podproperties-serviceaccountname)" : String,
  "[Volumes](#cfn-batch-jobdefinition-podproperties-volumes)" : [ EksVolume, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-podproperties-syntax.yaml"></a>

```
  [Containers](#cfn-batch-jobdefinition-podproperties-containers): 
    - EksContainer
  [DnsPolicy](#cfn-batch-jobdefinition-podproperties-dnspolicy): String
  [HostNetwork](#cfn-batch-jobdefinition-podproperties-hostnetwork): Boolean
  [ServiceAccountName](#cfn-batch-jobdefinition-podproperties-serviceaccountname): String
  [Volumes](#cfn-batch-jobdefinition-podproperties-volumes): 
    - EksVolume
```

## Properties<a name="aws-properties-batch-jobdefinition-podproperties-properties"></a>

`Containers`  <a name="cfn-batch-jobdefinition-podproperties-containers"></a>
The properties of the container that's used on the Amazon EKS pod\.  
*Required*: No  
*Type*: List of [EksContainer](aws-properties-batch-jobdefinition-ekscontainer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DnsPolicy`  <a name="cfn-batch-jobdefinition-podproperties-dnspolicy"></a>
The DNS policy for the pod\. The default value is `ClusterFirst`\. If the `hostNetwork` parameter is not specified, the default is `ClusterFirstWithHostNet`\. `ClusterFirst` indicates that any DNS query that does not match the configured cluster domain suffix is forwarded to the upstream nameserver inherited from the node\. If no value was specified for `dnsPolicy` in the [RegisterJobDefinition](https://docs.aws.amazon.com/batch/latest/APIReference/API_RegisterJobDefinition.html) API operation, then no value will be returned for `dnsPolicy` by either of [DescribeJobDefinitions](https://docs.aws.amazon.com/batch/latest/APIReference/API_DescribeJobDefinitions.html) or [DescribeJobs](https://docs.aws.amazon.com/batch/latest/APIReference/API_DescribeJobs.html) API operations\. The pod spec setting will contain either `ClusterFirst` or `ClusterFirstWithHostNet`, depending on the value of the `hostNetwork` parameter\. For more information, see [Pod's DNS policy](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#pod-s-dns-policy) in the *Kubernetes documentation*\.  
Valid values: `Default` \| `ClusterFirst` \| `ClusterFirstWithHostNet`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostNetwork`  <a name="cfn-batch-jobdefinition-podproperties-hostnetwork"></a>
Indicates if the pod uses the hosts' network IP address\. The default value is `true`\. Setting this to `false` enables the Kubernetes pod networking model\. Most AWS Batch workloads are egress\-only and don't require the overhead of IP allocation for each pod for incoming connections\. For more information, see [Host namespaces](https://kubernetes.io/docs/concepts/security/pod-security-policy/#host-namespaces) and [Pod networking](https://kubernetes.io/docs/concepts/workloads/pods/#pod-networking) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccountName`  <a name="cfn-batch-jobdefinition-podproperties-serviceaccountname"></a>
The name of the service account that's used to run the pod\. For more information, see [Kubernetes service accounts](https://docs.aws.amazon.com/eks/latest/userguide/service-accounts.html) and [Configure a Kubernetes service account to assume an IAM role](https://docs.aws.amazon.com/eks/latest/userguide/associate-service-account-role.html) in the *Amazon EKS User Guide* and [Configure service accounts for pods](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Volumes`  <a name="cfn-batch-jobdefinition-podproperties-volumes"></a>
Specifies the volumes for a job definition that uses Amazon EKS resources\.  
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-volumes.md) of [EksVolume](aws-properties-batch-jobdefinition-eksvolume.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)