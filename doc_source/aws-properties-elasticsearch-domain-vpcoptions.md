# Amazon Elasticsearch Service Domain VPCOptions<a name="aws-properties-elasticsearch-domain-vpcoptions"></a>

<a name="aws-properties-elasticsearch-domain-vpcoptions-description"></a>The `VPCOptions` property type specifies a virtual private cloud \(VPC\) configuration for an Amazon Elasticsearch Service \(Amazon ES\) domain\.

<a name="aws-properties-elasticsearch-domain-vpcoptions-inheritance"></a> `VPCOptions` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource\.

## Syntax<a name="aws-properties-elasticsearch-domain-vpcoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-vpcoptions-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-elasticsearch-domain-vpcoptions-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-elasticsearch-domain-vpcoptions-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticsearch-domain-vpcoptions-syntax.yaml"></a>

```
[SecurityGroupIds](#cfn-elasticsearch-domain-vpcoptions-securitygroupids): 
  - String
[SubnetIds](#cfn-elasticsearch-domain-vpcoptions-subnetids): 
  - String
```

## Properties<a name="aws-properties-elasticsearch-domain-vpcoptions-properties"></a>

`SecurityGroupIds`  <a name="cfn-elasticsearch-domain-vpcoptions-securitygroupids"></a>
The list of security group IDs that are associated with the VPC endpoints for the domain\. If you don't provide a security group ID, Amazon ES uses the default security group for the VPC\. To learn more, see [Security Groups for your VPC](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetIds`  <a name="cfn-elasticsearch-domain-vpcoptions-subnetids"></a>
A list of subnet IDs that are associated with the VPC endpoints for the domain\. If your domain has zone awareness enabled, you need to provide two subnet IDs, one per zone\. Otherwise, you only need to provide one\. To learn more, see [VPCs and Subnets](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html) in the *Amazon VPC User Guide*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-elasticsearch-domain-vpcoptions-seealso"></a>
+ [VPC Support for Amazon Elasticsearch Service Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-vpc.html) in the *Amazon Elasticsearch Service Developer Guide*