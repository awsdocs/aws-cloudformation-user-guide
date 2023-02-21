# AWS::Grafana::Workspace VpcConfiguration<a name="aws-properties-grafana-workspace-vpcconfiguration"></a>

The configuration settings for an Amazon VPC that contains data sources for your Grafana workspace to connect to\.

**Note**  
Provided `securityGroupIds` and `subnetIds` must be part of the same VPC\.

## Syntax<a name="aws-properties-grafana-workspace-vpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-grafana-workspace-vpcconfiguration-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-grafana-workspace-vpcconfiguration-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-grafana-workspace-vpcconfiguration-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-grafana-workspace-vpcconfiguration-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-grafana-workspace-vpcconfiguration-securitygroupids): 
    - String
  [SubnetIds](#cfn-grafana-workspace-vpcconfiguration-subnetids): 
    - String
```

## Properties<a name="aws-properties-grafana-workspace-vpcconfiguration-properties"></a>

`SecurityGroupIds`  <a name="cfn-grafana-workspace-vpcconfiguration-securitygroupids"></a>
The list of Amazon EC2 security group IDs attached to the Amazon VPC for your Grafana workspace to connect\. Duplicates not allowed\.  
*Array Members*: Minimum number of 1 items\. Maximum number of 5 items\.  
*Length*: Minimum length of 0\. Maximum length of 255\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-grafana-workspace-vpcconfiguration-subnetids"></a>
The list of Amazon EC2 subnet IDs created in the Amazon VPC for your Grafana workspace to connect\. Duplicates not allowed\.  
*Array Members*: Minimum number of 2 items\. Maximum number of 6 items\.  
*Length*: Minimum length of 0\. Maximum length of 255\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)