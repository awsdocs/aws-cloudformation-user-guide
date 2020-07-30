# AWS::MSK::Cluster BrokerNodeGroupInfo<a name="aws-properties-msk-cluster-brokernodegroupinfo"></a>

The setup to be used for brokers in the cluster\.

## Syntax<a name="aws-properties-msk-cluster-brokernodegroupinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-brokernodegroupinfo-syntax.json"></a>

```
{
  "[BrokerAZDistribution](#cfn-msk-cluster-brokernodegroupinfo-brokerazdistribution)" : String,
  "[ClientSubnets](#cfn-msk-cluster-brokernodegroupinfo-clientsubnets)" : [ String, ... ],
  "[InstanceType](#cfn-msk-cluster-brokernodegroupinfo-instancetype)" : String,
  "[SecurityGroups](#cfn-msk-cluster-brokernodegroupinfo-securitygroups)" : [ String, ... ],
  "[StorageInfo](#cfn-msk-cluster-brokernodegroupinfo-storageinfo)" : StorageInfo
}
```

### YAML<a name="aws-properties-msk-cluster-brokernodegroupinfo-syntax.yaml"></a>

```
  [BrokerAZDistribution](#cfn-msk-cluster-brokernodegroupinfo-brokerazdistribution): String
  [ClientSubnets](#cfn-msk-cluster-brokernodegroupinfo-clientsubnets): 
    - String
  [InstanceType](#cfn-msk-cluster-brokernodegroupinfo-instancetype): String
  [SecurityGroups](#cfn-msk-cluster-brokernodegroupinfo-securitygroups): 
    - String
  [StorageInfo](#cfn-msk-cluster-brokernodegroupinfo-storageinfo): 
    StorageInfo
```

## Properties<a name="aws-properties-msk-cluster-brokernodegroupinfo-properties"></a>

`BrokerAZDistribution`  <a name="cfn-msk-cluster-brokernodegroupinfo-brokerazdistribution"></a>
The distribution of broker nodes across Availability Zones\. This is an optional parameter\. If you don't specify it, Amazon MSK gives it the value `DEFAULT`\. You can also explicitly set this parameter to the value `DEFAULT`\. No other values are currently allowed\.  
Amazon MSK distributes the broker nodes evenly across the Availability Zones that correspond to the subnets that you provide when you create the cluster\.  
To create a cluster, specify exactly two subnets if you are using one of the following Regions: South America \(São Paulo\), Canada \(Central\), or US West \(N\. California\)\. For other Regions where Amazon MSK is available, you can specify either two or three subnets\. The subnets that you specify must be in distinct Availability Zones\.  
Client subnets can't be in Availability Zone us\-east\-1e\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientSubnets`  <a name="cfn-msk-cluster-brokernodegroupinfo-clientsubnets"></a>
The list of subnets to connect to in the client virtual private cloud \(VPC\)\. AWS creates elastic network interfaces inside these subnets\. Client applications use elastic network interfaces to produce and consume data\.   
Specify exactly two subnets if you are using the US West \(N\. California\) Region\. For other Regions where Amazon MSK is available, you can specify either two or three subnets\. The subnets that you specify must be in distinct Availability Zones\. When you create a cluster, Amazon MSK distributes the broker nodes evenly across the subnets that you specify\.  
Client subnets can't be in Availability Zone us\-east\-1e\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-msk-cluster-brokernodegroupinfo-instancetype"></a>
The type of Amazon EC2 instances to use for brokers\. The following instance types are allowed: kafka\.m5\.large, kafka\.m5\.xlarge, kafka\.m5\.2xlarge, kafka\.m5\.4xlarge, kafka\.m5\.8xlarge, kafka\.m5\.12xlarge, kafka\.m5\.16xlarge, and kafka\.m5\.24xlarge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-msk-cluster-brokernodegroupinfo-securitygroups"></a>
The AWS security groups to associate with the elastic network interfaces in order to specify who can connect to and communicate with the Amazon MSK cluster\. If you don't specify a security group, Amazon MSK uses the default security group associated with the VPC\. If you specify security groups that were shared with you, you must ensure that you have permissions to them\. Specifically, you need the `ec2:DescribeSecurityGroups` permission\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageInfo`  <a name="cfn-msk-cluster-brokernodegroupinfo-storageinfo"></a>
Contains information about storage volumes attached to MSK broker nodes\.  
*Required*: No  
*Type*: [StorageInfo](aws-properties-msk-cluster-storageinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)