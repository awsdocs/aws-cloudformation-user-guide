# AWS::Elasticsearch::Domain VPCOptions<a name="aws-properties-elasticsearch-domain-vpcoptions"></a>

The virtual private cloud \(VPC\) configuration for the OpenSearch Service domain\. For more information, see [Launching your Amazon OpenSearch Service domains using a VPC](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html) in the *Amazon OpenSearch Service Developer Guide*\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

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
The list of security group IDs that are associated with the VPC endpoints for the domain\. If you don't provide a security group ID, OpenSearch Service uses the default security group for the VPC\. To learn more, see [Security groups for your VPC ](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-elasticsearch-domain-vpcoptions-subnetids"></a>
Provide one subnet ID for each Availability Zone that your domain uses\. For example, you must specify three subnet IDs for a three Availability Zone domain\. To learn more, see [VPCs and subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html) in the *Amazon VPC User Guide*\.  
Required if you're creating your domain inside a VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-elasticsearch-domain-vpcoptions--seealso"></a>
+ [Launching your Amazon OpenSearch Service domains within a VPC](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html) in the *Amazon OpenSearch Service Developer Guide*\.

