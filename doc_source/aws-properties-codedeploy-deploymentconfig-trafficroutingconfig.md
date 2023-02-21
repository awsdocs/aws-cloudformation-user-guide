# AWS::CodeDeploy::DeploymentConfig TrafficRoutingConfig<a name="aws-properties-codedeploy-deploymentconfig-trafficroutingconfig"></a>

The configuration that specifies how traffic is shifted from one version of a Lambda function to another version during an AWS Lambda deployment, or from one Amazon ECS task set to another during an Amazon ECS deployment\.

## Syntax<a name="aws-properties-codedeploy-deploymentconfig-trafficroutingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentconfig-trafficroutingconfig-syntax.json"></a>

```
{
  "[TimeBasedCanary](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedcanary)" : TimeBasedCanary,
  "[TimeBasedLinear](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear)" : TimeBasedLinear,
  "[Type](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-type)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentconfig-trafficroutingconfig-syntax.yaml"></a>

```
  [TimeBasedCanary](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedcanary): 
    TimeBasedCanary
  [TimeBasedLinear](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear): 
    TimeBasedLinear
  [Type](#cfn-codedeploy-deploymentconfig-trafficroutingconfig-type): String
```

## Properties<a name="aws-properties-codedeploy-deploymentconfig-trafficroutingconfig-properties"></a>

`TimeBasedCanary`  <a name="cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedcanary"></a>
A configuration that shifts traffic from one version of a Lambda function or ECS task set to another in two increments\. The original and target Lambda function versions or ECS task sets are specified in the deployment's AppSpec file\.  
*Required*: No  
*Type*: [TimeBasedCanary](aws-properties-codedeploy-deploymentconfig-timebasedcanary.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeBasedLinear`  <a name="cfn-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear"></a>
A configuration that shifts traffic from one version of a Lambda function or Amazon ECS task set to another in equal increments, with an equal number of minutes between each increment\. The original and target Lambda function versions or Amazon ECS task sets are specified in the deployment's AppSpec file\.  
*Required*: No  
*Type*: [TimeBasedLinear](aws-properties-codedeploy-deploymentconfig-timebasedlinear.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-codedeploy-deploymentconfig-trafficroutingconfig-type"></a>
The type of traffic shifting \(`TimeBasedCanary` or `TimeBasedLinear`\) used by a deployment configuration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AllAtOnce | TimeBasedCanary | TimeBasedLinear`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)