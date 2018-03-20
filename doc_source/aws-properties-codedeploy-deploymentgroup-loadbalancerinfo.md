# AWS CodeDeploy DeploymentGroup LoadBalancerInfo<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo"></a>

The `LoadBalancerInfo` property type specifies information about the load balancer or target group used for an AWS CodeDeploy deployment group\. For more information, see [ Integrating AWS CodeDeploy with Elastic Load Balancing](http://docs.aws.amazon.com/codedeploy/latest/userguide/integrations-aws-elastic-load-balancing.html) in the *AWS CodeDeploy User Guide*\.

For AWS CloudFormation to use the properties specified in `LoadBalancerInfo`, the `DeploymentStyle.DeploymentOption` property must be set to `WITH_TRAFFIC_CONTROL`\. If `DeploymentStyle.DeploymentOption` is not set to `WITH_TRAFFIC_CONTROL`, AWS CloudFormation ignores any settings specified in `LoadBalancerInfo`\.

**Note**  
AWS CloudFormation supports blue/green deployments on AWS Lambda compute platforms only\.

 `LoadBalancerInfo` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax.json"></a>

```
{
  "[ElbInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist)" : [ [*ELBInfo*](aws-properties-codedeploy-deploymentgroup-elbinfo.md), ... ],
  "[TargetGroupInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist)" : [ [*TargetGroupInfo*](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md), ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax.yaml"></a>

```
[ElbInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist): 
  - [*ELBInfo*](aws-properties-codedeploy-deploymentgroup-elbinfo.md)
[TargetGroupInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist): 
  - [*TargetGroupInfo*](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md)
```

### Properties<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-properties"></a>

`ElbInfoList`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist"></a>
Information about the Elastic Load Balancing load balancer to use in the deployment\.  
Conditional: You must specify either `ElbInfoList` or `TargetGroupInfoList`, but not both\.  
 *Required*: No  
 *Type*: List of [AWS CodeDeploy DeploymentGroup ELBInfo](aws-properties-codedeploy-deploymentgroup-elbinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetGroupInfoList`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist"></a>
information about the target groups to use in the deployment\. Instances are registered as targets in a target group, and traffic is routed to the target group\.   
Conditional: You must specify either `ElbInfoList` or `TargetGroupInfoList`, but not both\.  
 *Required*: No  
 *Type*: List of [AWS CodeDeploy DeploymentGroup TargetGroupInfo](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 