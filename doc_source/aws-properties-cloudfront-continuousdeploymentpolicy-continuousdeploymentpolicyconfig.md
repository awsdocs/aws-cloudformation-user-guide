# AWS::CloudFront::ContinuousDeploymentPolicy ContinuousDeploymentPolicyConfig<a name="aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig"></a>

Contains the configuration for a continuous deployment policy\.

## Syntax<a name="aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-syntax.json"></a>

```
{
  "[Enabled](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-enabled)" : Boolean,
  "[StagingDistributionDnsNames](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-stagingdistributiondnsnames)" : [ String, ... ],
  "[TrafficConfig](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-trafficconfig)" : TrafficConfig
}
```

### YAML<a name="aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-syntax.yaml"></a>

```
  [Enabled](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-enabled): Boolean
  [StagingDistributionDnsNames](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-stagingdistributiondnsnames): 
    - String
  [TrafficConfig](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-trafficconfig): 
    TrafficConfig
```

## Properties<a name="aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-properties"></a>

`Enabled`  <a name="cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-enabled"></a>
A Boolean that indicates whether this continuous deployment policy is enabled \(in effect\)\. When this value is `true`, this policy is enabled and in effect\. When this value is `false`, this policy is not enabled and has no effect\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StagingDistributionDnsNames`  <a name="cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-stagingdistributiondnsnames"></a>
The CloudFront domain name of the staging distribution\. For example: `d111111abcdef8.cloudfront.net`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficConfig`  <a name="cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig-trafficconfig"></a>
Contains the parameters for routing production traffic from your primary to staging distributions\.  
*Required*: No  
*Type*: [TrafficConfig](aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)