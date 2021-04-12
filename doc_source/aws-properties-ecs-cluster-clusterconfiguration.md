# AWS::ECS::Cluster ClusterConfiguration<a name="aws-properties-ecs-cluster-clusterconfiguration"></a>

The execute command configuration for the cluster\.

## Syntax<a name="aws-properties-ecs-cluster-clusterconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-cluster-clusterconfiguration-syntax.json"></a>

```
{
  "[ExecuteCommandConfiguration](#cfn-ecs-cluster-clusterconfiguration-executecommandconfiguration)" : ExecuteCommandConfiguration
}
```

### YAML<a name="aws-properties-ecs-cluster-clusterconfiguration-syntax.yaml"></a>

```
  [ExecuteCommandConfiguration](#cfn-ecs-cluster-clusterconfiguration-executecommandconfiguration): 
    ExecuteCommandConfiguration
```

## Properties<a name="aws-properties-ecs-cluster-clusterconfiguration-properties"></a>

`ExecuteCommandConfiguration`  <a name="cfn-ecs-cluster-clusterconfiguration-executecommandconfiguration"></a>
The details of the execute command configuration\.  
*Required*: No  
*Type*: [ExecuteCommandConfiguration](aws-properties-ecs-cluster-executecommandconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)