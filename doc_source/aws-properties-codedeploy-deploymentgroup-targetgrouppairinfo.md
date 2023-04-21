# AWS::CodeDeploy::DeploymentGroup TargetGroupPairInfo<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo"></a>

<a name="aws-properties-codedeploy-deploymentgroup-targetgrouppairinfo-description"></a>The `TargetGroupPairInfo` property type specifies Property description not available\. for an [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md)\.

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
Property description not available\.  
*Required*: No  
*Type*: [TrafficRoute](aws-properties-codedeploy-deploymentgroup-trafficroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroups`  <a name="cfn-codedeploy-deploymentgroup-targetgrouppairinfo-targetgroups"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [TargetGroupInfo](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TestTrafficRoute`  <a name="cfn-codedeploy-deploymentgroup-targetgrouppairinfo-testtrafficroute"></a>
Property description not available\.  
*Required*: No  
*Type*: [TrafficRoute](aws-properties-codedeploy-deploymentgroup-trafficroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)