# AWS::CodeDeploy::DeploymentGroup ECSService<a name="aws-properties-codedeploy-deploymentgroup-ecsservice"></a>

 Contains the service and cluster names used to identify an Amazon ECS deployment's target\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-ecsservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ecsservice-syntax.json"></a>

```
{
  "[ClusterName](#cfn-codedeploy-deploymentgroup-ecsservice-clustername)" : String,
  "[ServiceName](#cfn-codedeploy-deploymentgroup-ecsservice-servicename)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ecsservice-syntax.yaml"></a>

```
  [ClusterName](#cfn-codedeploy-deploymentgroup-ecsservice-clustername): String
  [ServiceName](#cfn-codedeploy-deploymentgroup-ecsservice-servicename): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-ecsservice-properties"></a>

`ClusterName`  <a name="cfn-codedeploy-deploymentgroup-ecsservice-clustername"></a>
 The name of the cluster that the Amazon ECS service is associated with\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-codedeploy-deploymentgroup-ecsservice-servicename"></a>
 The name of the target Amazon ECS service\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)