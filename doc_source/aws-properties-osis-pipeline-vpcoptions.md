# AWS::OSIS::Pipeline VpcOptions<a name="aws-properties-osis-pipeline-vpcoptions"></a>

Options that specify the subnets and security groups for an OpenSearch Ingestion VPC endpoint\.

## Syntax<a name="aws-properties-osis-pipeline-vpcoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-osis-pipeline-vpcoptions-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-osis-pipeline-vpcoptions-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-osis-pipeline-vpcoptions-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-osis-pipeline-vpcoptions-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-osis-pipeline-vpcoptions-securitygroupids): 
    - String
  [SubnetIds](#cfn-osis-pipeline-vpcoptions-subnetids): 
    - String
```

## Properties<a name="aws-properties-osis-pipeline-vpcoptions-properties"></a>

`SecurityGroupIds`  <a name="cfn-osis-pipeline-vpcoptions-securitygroupids"></a>
A list of security groups associated with the VPC endpoint\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `12`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-osis-pipeline-vpcoptions-subnetids"></a>
A list of subnet IDs associated with the VPC endpoint\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `12`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)