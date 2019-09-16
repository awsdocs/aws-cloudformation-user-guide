# AWS::CodeDeploy::DeploymentGroup DeploymentStyle<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle"></a>

Information about the type of deployment, either in\-place or blue/green, you want to run and whether to route deployment traffic behind a load balancer\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-syntax.json"></a>

```
{
  "[DeploymentOption](#cfn-codedeploy-deploymentgroup-deploymentstyle-deploymentoption)" : String,
  "[DeploymentType](#cfn-codedeploy-deploymentgroup-deploymentstyle-deploymenttype)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-syntax.yaml"></a>

```
  [DeploymentOption](#cfn-codedeploy-deploymentgroup-deploymentstyle-deploymentoption): String
  [DeploymentType](#cfn-codedeploy-deploymentgroup-deploymentstyle-deploymenttype): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-properties"></a>

`DeploymentOption`  <a name="cfn-codedeploy-deploymentgroup-deploymentstyle-deploymentoption"></a>
Indicates whether to route deployment traffic behind a load balancer\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `WITHOUT_TRAFFIC_CONTROL | WITH_TRAFFIC_CONTROL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-codedeploy-deploymentgroup-deploymentstyle-deploymenttype"></a>
Indicates whether to run an in\-place or blue/green deployment\.  
AWS CloudFormation supports blue/green deployments on AWS Lambda compute platforms only\. For more information about deploying on an AWS Lambda compute platform, see [ Deployments on an AWS Lambda Compute Platform](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-steps.html#deployment-steps-lambda) in the *AWS CodeDeploy User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `BLUE_GREEN | IN_PLACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle--seealso"></a>
+  [EC2TagFilter](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagFilter.html) in the *AWS CodeDeploy API Reference*\.