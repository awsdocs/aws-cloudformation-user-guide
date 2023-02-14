# AWS::CodeDeploy::DeploymentConfig TimeBasedLinear<a name="aws-properties-codedeploy-deploymentconfig-timebasedlinear"></a>

A configuration that shifts traffic from one version of a Lambda function or ECS task set to another in equal increments, with an equal number of minutes between each increment\. The original and target Lambda function versions or ECS task sets are specified in the deployment's AppSpec file\.

## Syntax<a name="aws-properties-codedeploy-deploymentconfig-timebasedlinear-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentconfig-timebasedlinear-syntax.json"></a>

```
{
  "[LinearInterval](#cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearinterval)" : Integer,
  "[LinearPercentage](#cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearpercentage)" : Integer
}
```

### YAML<a name="aws-properties-codedeploy-deploymentconfig-timebasedlinear-syntax.yaml"></a>

```
  [LinearInterval](#cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearinterval): Integer
  [LinearPercentage](#cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearpercentage): Integer
```

## Properties<a name="aws-properties-codedeploy-deploymentconfig-timebasedlinear-properties"></a>

`LinearInterval`  <a name="cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearinterval"></a>
The number of minutes between each incremental traffic shift of a `TimeBasedLinear` deployment\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LinearPercentage`  <a name="cfn-properties-codedeploy-deploymentconfig-trafficroutingconfig-timebasedlinear-linearpercentage"></a>
The percentage of traffic that is shifted at the start of each increment of a `TimeBasedLinear` deployment\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)