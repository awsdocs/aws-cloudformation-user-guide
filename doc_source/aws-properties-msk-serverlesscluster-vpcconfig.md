# AWS::MSK::ServerlessCluster VpcConfig<a name="aws-properties-msk-serverlesscluster-vpcconfig"></a>

Specifies information about subnets and security groups for the VPC that your clients will use to connect with the serverless cluster\.

## Syntax<a name="aws-properties-msk-serverlesscluster-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-serverlesscluster-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroups](#cfn-msk-serverlesscluster-vpcconfig-securitygroups)" : [ String, ... ],
  "[SubnetIds](#cfn-msk-serverlesscluster-vpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-msk-serverlesscluster-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroups](#cfn-msk-serverlesscluster-vpcconfig-securitygroups): 
    - String
  [SubnetIds](#cfn-msk-serverlesscluster-vpcconfig-subnetids): 
    - String
```

## Properties<a name="aws-properties-msk-serverlesscluster-vpcconfig-properties"></a>

`SecurityGroups`  <a name="cfn-msk-serverlesscluster-vpcconfig-securitygroups"></a>
Specifies up to five security groups that control inbound and outbound traffic for the serverless cluster\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-msk-serverlesscluster-vpcconfig-subnetids"></a>
A list of subnets in at least two different Availability Zones that host your client applications\. We recommend that you specify a backup subnet in a different Availability Zone for failover in case of an outage\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)