# AWS::CodeDeploy::DeploymentGroup TargetGroupPairInfo<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo"></a>

 Information about two target groups and how traffic is routed during an Amazon ECS deployment\. An optional test traffic route can be specified\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo-syntax.json"></a>

```
{
  "[ProdTrafficRoute](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-prodtrafficroute)" : TrafficRoute,
  "[TargetGroups](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-targetgroups)" : [ TargetGroupInfo, ... ],
  "[TestTrafficRoute](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-testtrafficroute)" : TrafficRoute
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo-syntax.yaml"></a>

```
  [ProdTrafficRoute](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-prodtrafficroute): 
    TrafficRoute
  [TargetGroups](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-targetgroups): 
    - TargetGroupInfo
  [TestTrafficRoute](#cfn-codedeploy-deploymentgroup-targetgrouppairinfo-testtrafficroute): 
    TrafficRoute
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo-properties"></a>

`ProdTrafficRoute`  <a name="cfn-codedeploy-deploymentgroup-targetgrouppairinfo-prodtrafficroute"></a>
 The path used by a load balancer to route production traffic when an Amazon ECS deployment is complete\.   
*Required*: No  
*Type*: [TrafficRoute](aws-properties-codedeploy-deploymentgroup-trafficroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroups`  <a name="cfn-codedeploy-deploymentgroup-targetgrouppairinfo-targetgroups"></a>
 One pair of target groups\. One is associated with the original task set\. The second is associated with the task set that serves traffic after the deployment is complete\.   
*Required*: No  
*Type*: List of [TargetGroupInfo](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TestTrafficRoute`  <a name="cfn-codedeploy-deploymentgroup-targetgrouppairinfo-testtrafficroute"></a>
 An optional path used by a load balancer to route test traffic after an Amazon ECS deployment\. Validation can occur while test traffic is served during a deployment\.   
*Required*: No  
*Type*: [TrafficRoute](aws-properties-codedeploy-deploymentgroup-trafficroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)