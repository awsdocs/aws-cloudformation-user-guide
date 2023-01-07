# AWS::CodeDeploy::DeploymentGroup TargetGroupInfo<a name="aws-properties-codedeploy-deploymentgroup-targetgroupinfo"></a>

The `TargetGroupInfo` property type specifies information about a target group in Elastic Load Balancing to use in a deployment\. Instances are registered as targets in a target group, and traffic is routed to the target group\. For more information, see [ TargetGroupInfo](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_TargetGroupInfo.html) in the *AWS CodeDeploy API Reference* 

If you specify the `TargetGroupInfo` property, the `DeploymentStyle.DeploymentOption` property must be set to `WITH_TRAFFIC_CONTROL` for CodeDeploy to route your traffic using the specified target groups\.

 `TargetGroupInfo` is a property of the [LoadBalancerInfo](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codedeploy-deploymentgroup-loadbalancerinfo.html) property type\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-targetgroupinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-targetgroupinfo-syntax.json"></a>

```
{
  "[Name](#cfn-codedeploy-deploymentgroup-targetgroupinfo-name)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-targetgroupinfo-syntax.yaml"></a>

```
  [Name](#cfn-codedeploy-deploymentgroup-targetgroupinfo-name): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-targetgroupinfo-properties"></a>

`Name`  <a name="cfn-codedeploy-deploymentgroup-targetgroupinfo-name"></a>
For blue/green deployments, the name of the target group that instances in the original environment are deregistered from, and instances in the replacement environment registered with\. For in\-place deployments, the name of the target group that instances are deregistered from, so they are not serving traffic during a deployment, and then re\-registered with after the deployment completes\. No duplicates allowed\.  
AWS CloudFormation supports blue/green deployments on AWS Lambda compute platforms only\.
This value cannot exceed 32 characters, so you should use the `Name` property of the target group, or the `TargetGroupName` attribute with the `Fn::GetAtt` intrinsic function, as shown in the following example\. Don't use the group's Amazon Resource Name \(ARN\) or `TargetGroupFullName` attribute\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)