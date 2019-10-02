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
  "[StorageInfo](#cfn-msk-cluster-brokernodegroupinfo-storageinfo)" : [StorageInfo](aws-properties-msk-cluster-storageinfo.md)
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
    [StorageInfo](aws-properties-msk-cluster-storageinfo.md)
```

## Properties<a name="aws-properties-msk-cluster-brokernodegroupinfo-properties"></a>

`BrokerAZDistribution`  <a name="cfn-msk-cluster-brokernodegroupinfo-brokerazdistribution"></a>
The distribution of broker nodes across Availability Zones\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientSubnets`  <a name="cfn-msk-cluster-brokernodegroupinfo-clientsubnets"></a>
The list of subnets to connect to in the client virtual private cloud \(VPC\)\. AWS creates elastic network interfaces inside these subnets\. Client applications use elastic network interfaces to produce and consume data\. Client subnets can't be in Availability Zone us\-east\-1e\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-msk-cluster-brokernodegroupinfo-instancetype"></a>
The type of Amazon EC2 instances to use for Kafka brokers\. The following instance types are allowed: kafka\.m5\.large, kafka\.m5\.xlarge, kafka\.m5\.2xlarge, kafka\.m5\.4xlarge, kafka\.m5\.12xlarge, and kafka\.m5\.24xlarge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-msk-cluster-brokernodegroupinfo-securitygroups"></a>
The AWS security groups to associate with the elastic network interfaces in order to specify who can connect to and communicate with the Amazon MSK cluster\. If you don't specify a security group, Amazon MSK uses the default security group associated with the VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageInfo`  <a name="cfn-msk-cluster-brokernodegroupinfo-storageinfo"></a>
Contains information about storage volumes attached to MSK broker nodes\.  
*Required*: No  
*Type*: [StorageInfo](aws-properties-msk-cluster-storageinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-2`
