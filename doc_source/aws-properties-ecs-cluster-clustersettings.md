# AWS::ECS::Cluster ClusterSettings<a name="aws-properties-ecs-cluster-clustersettings"></a>

The settings to use when creating a cluster\. This parameter is used to enable CloudWatch Container Insights for a cluster\.

## Syntax<a name="aws-properties-ecs-cluster-clustersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-cluster-clustersettings-syntax.json"></a>

```
{
  "[Name](#cfn-ecs-cluster-clustersettings-name)" : String,
  "[Value](#cfn-ecs-cluster-clustersettings-value)" : String
}
```

### YAML<a name="aws-properties-ecs-cluster-clustersettings-syntax.yaml"></a>

```
  [Name](#cfn-ecs-cluster-clustersettings-name): String
  [Value](#cfn-ecs-cluster-clustersettings-value): String
```

## Properties<a name="aws-properties-ecs-cluster-clustersettings-properties"></a>

`Name`  <a name="cfn-ecs-cluster-clustersettings-name"></a>
The name of the cluster setting\. The only supported value is `containerInsights`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `containerInsights`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ecs-cluster-clustersettings-value"></a>
The value to set for the cluster setting\. The supported values are `enabled` and `disabled`\. If `enabled` is specified, CloudWatch Container Insights will be enabled for the cluster, otherwise it will be disabled unless the `containerInsights` account setting is enabled\. If a cluster value is specified, it will override the `containerInsights` value set with [PutAccountSetting](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_PutAccountSetting.html) or [PutAccountSettingDefault](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_PutAccountSettingDefault.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)