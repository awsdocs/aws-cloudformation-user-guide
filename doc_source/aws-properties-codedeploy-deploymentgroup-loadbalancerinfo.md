# AWS::CodeDeploy::DeploymentGroup LoadBalancerInfo<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo"></a>

The `LoadBalancerInfo` property type specifies information about the load balancer or target group used for an AWS CodeDeploy deployment group\. For more information, see [ Integrating CodeDeploy with Elastic Load Balancing ](https://docs.aws.amazon.com/codedeploy/latest/userguide/integrations-aws-elastic-load-balancing.html) in the *AWS CodeDeploy User Guide*\.

For AWS CloudFormation to use the properties specified in `LoadBalancerInfo`, the `DeploymentStyle.DeploymentOption` property must be set to `WITH_TRAFFIC_CONTROL`\. If `DeploymentStyle.DeploymentOption` is not set to `WITH_TRAFFIC_CONTROL`, AWS CloudFormation ignores any settings specified in `LoadBalancerInfo`\.

**Note**  
AWS CloudFormation supports blue/green deployments on the AWS Lambda compute platform only\.

 `LoadBalancerInfo` is a property of the [DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax.json"></a>

```
{
  "[ElbInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist)" : [ ELBInfo, ... ],
  "[TargetGroupInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist)" : [ TargetGroupInfo, ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-syntax.yaml"></a>

```
  [ElbInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist): 
    - ELBInfo
  [TargetGroupInfoList](#cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist): 
    - TargetGroupInfo
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-loadbalancerinfo-properties"></a>

`ElbInfoList`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo-elbinfolist"></a>
An array that contains information about the load balancer to use for load balancing in a deployment\. In Elastic Load Balancing, load balancers are used with Classic Load Balancers\.  
 Adding more than one load balancer to the array is not supported\. 
*Required*: No  
*Type*: List of [ELBInfo](aws-properties-codedeploy-deploymentgroup-elbinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupInfoList`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo-targetgroupinfolist"></a>
An array that contains information about the target group to use for load balancing in a deployment\. In Elastic Load Balancing, target groups are used with Application Load Balancers\.  
 Adding more than one target group to the array is not supported\. 
*Required*: Conditional  
*Type*: List of [TargetGroupInfo](aws-properties-codedeploy-deploymentgroup-targetgroupinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)