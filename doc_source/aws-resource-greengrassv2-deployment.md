# AWS::GreengrassV2::Deployment<a name="aws-resource-greengrassv2-deployment"></a>

<a name="aws-resource-greengrassv2-deployment-description"></a>The `AWS::GreengrassV2::Deployment` resource Not currently supported by AWS CloudFormation\. for GreengrassV2\.

## Syntax<a name="aws-resource-greengrassv2-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrassv2-deployment-syntax.json"></a>

```
{
  "Type" : "AWS::GreengrassV2::Deployment",
  "Properties" : {
      "[Components](#cfn-greengrassv2-deployment-components)" : {Key : Value, ...},
      "[DeploymentName](#cfn-greengrassv2-deployment-deploymentname)" : String,
      "[DeploymentPolicies](#cfn-greengrassv2-deployment-deploymentpolicies)" : DeploymentPolicies,
      "[IotJobConfiguration](#cfn-greengrassv2-deployment-iotjobconfiguration)" : DeploymentIoTJobConfiguration,
      "[Tags](#cfn-greengrassv2-deployment-tags)" : {Key : Value, ...},
      "[TargetArn](#cfn-greengrassv2-deployment-targetarn)" : String
    }
}
```

### YAML<a name="aws-resource-greengrassv2-deployment-syntax.yaml"></a>

```
Type: AWS::GreengrassV2::Deployment
Properties: 
  [Components](#cfn-greengrassv2-deployment-components): 
    Key : Value
  [DeploymentName](#cfn-greengrassv2-deployment-deploymentname): String
  [DeploymentPolicies](#cfn-greengrassv2-deployment-deploymentpolicies): 
    DeploymentPolicies
  [IotJobConfiguration](#cfn-greengrassv2-deployment-iotjobconfiguration): 
    DeploymentIoTJobConfiguration
  [Tags](#cfn-greengrassv2-deployment-tags): 
    Key : Value
  [TargetArn](#cfn-greengrassv2-deployment-targetarn): String
```

## Properties<a name="aws-resource-greengrassv2-deployment-properties"></a>

`Components`  <a name="cfn-greengrassv2-deployment-components"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Map of [ComponentDeploymentSpecification](aws-properties-greengrassv2-deployment-componentdeploymentspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentName`  <a name="cfn-greengrassv2-deployment-deploymentname"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentPolicies`  <a name="cfn-greengrassv2-deployment-deploymentpolicies"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DeploymentPolicies](aws-properties-greengrassv2-deployment-deploymentpolicies.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IotJobConfiguration`  <a name="cfn-greengrassv2-deployment-iotjobconfiguration"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DeploymentIoTJobConfiguration](aws-properties-greengrassv2-deployment-deploymentiotjobconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-greengrassv2-deployment-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-greengrassv2-deployment-targetarn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrassv2-deployment-return-values"></a>

### Ref<a name="aws-resource-greengrassv2-deployment-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-greengrassv2-deployment-return-values-fn--getatt"></a>

#### <a name="aws-resource-greengrassv2-deployment-return-values-fn--getatt-fn--getatt"></a>

`DeploymentId`  <a name="DeploymentId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.