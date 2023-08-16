# AWS::CloudFront::ContinuousDeploymentPolicy TrafficConfig<a name="aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig"></a>

The traffic configuration of your continuous deployment\.

## Syntax<a name="aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig-syntax.json"></a>

```
{
  "[SingleHeaderConfig](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleheaderconfig)" : SingleHeaderConfig,
  "[SingleWeightConfig](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleweightconfig)" : SingleWeightConfig,
  "[Type](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-type)" : String
}
```

### YAML<a name="aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig-syntax.yaml"></a>

```
  [SingleHeaderConfig](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleheaderconfig): 
    SingleHeaderConfig
  [SingleWeightConfig](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleweightconfig): 
    SingleWeightConfig
  [Type](#cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-type): String
```

## Properties<a name="aws-properties-cloudfront-continuousdeploymentpolicy-trafficconfig-properties"></a>

`SingleHeaderConfig`  <a name="cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleheaderconfig"></a>
Determines which HTTP requests are sent to the staging distribution\.  
*Required*: No  
*Type*: [SingleHeaderConfig](aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleWeightConfig`  <a name="cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-singleweightconfig"></a>
Contains the percentage of traffic to send to the staging distribution\.  
*Required*: No  
*Type*: [SingleWeightConfig](aws-properties-cloudfront-continuousdeploymentpolicy-singleweightconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-cloudfront-continuousdeploymentpolicy-trafficconfig-type"></a>
The type of traffic configuration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SingleHeader | SingleWeight`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)