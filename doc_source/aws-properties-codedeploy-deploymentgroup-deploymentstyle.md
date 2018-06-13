# AWS CodeDeploy DeploymentGroup DeploymentStyle<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle"></a>

The `DeploymentStyle` property type specifies the type of AWS CodeDeploy deployment that you want to run and whether to route deployment traffic behind a load balancer\.

`DeploymentStyle` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource\.

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
 *Valid values*: `WITH_TRAFFIC_CONTROL` or `WITHOUT_TRAFFIC_CONTROL`  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeploymentType`  <a name="cfn-codedeploy-deploymentgroup-deploymentstyle-deploymenttype"></a>
Indicates whether to run an in\-place or blue/green deployment\.  
AWS CloudFormation supports blue/green deployments on AWS Lambda compute platforms only\. For more information about deploying on a AWS Lambda compute platform, see [ Deployments on an AWS Lambda Compute Platform](http://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-steps.html#deployment-steps-lambda) in the *AWS CodeDeploy User Guide*\.  
 *Required*: No  
 *Type*: String  
 *Valid values*: `IN_PLACE` or `BLUE_GREEN`  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-seealso"></a>
+ [ DeploymentStyle](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_DeploymentStyle.html) in the *AWS CodeDeploy API Reference*

## Example<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-examples"></a>

The following example creates deployment group with a `BLUE_GREEN` deployment type\.

### JSON<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-example.json"></a>

```
"CodeDeployDeploymentGroup": {
  "Type": "AWS::CodeDeploy::DeploymentGroup",
  "Properties": {
    "ApplicationName": {
      "Ref": "CodeDeployApplication"
    },
    "DeploymentConfigName": "CodeDeployDefault.LambdaCanary10Percent5Minutes",
    "DeploymentStyle": {
      "DeploymentType": "BLUE_GREEN",
      "DeploymentOption": "WITH_TRAFFIC_CONTROL"
    },
    "ServiceRoleArn": {
      "Fn::GetAtt": [
        "CodeDeployServiceRole",
        "Arn"
      ]
    }
  }
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle.yaml"></a>

```
CodeDeployDeploymentGroup:
  Type: 'AWS::CodeDeploy::DeploymentGroup'
  Properties:
    ApplicationName: !Ref CodeDeployApplication
    DeploymentConfigName: CodeDeployDefault.LambdaCanary10Percent5Minutes
    DeploymentStyle:
      DeploymentType: BLUE_GREEN
      DeploymentOption: WITH_TRAFFIC_CONTROL
    ServiceRoleArn: !GetAtt CodeDeployServiceRole.Arn
```

## See Also<a name="aws-properties-codedeploy-deploymentgroup-deploymentstyle-seealso"></a>
+ [ DeploymentStyle](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_DeploymentStyle.html) in the *AWS CodeDeploy API Reference*