# AWS::GreengrassV2::Deployment<a name="aws-resource-greengrassv2-deployment"></a>

Creates a continuous deployment for a target, which is a AWS IoT Greengrass core device or group of core devices\. When you add a new core device to a group of core devices that has a deployment, AWS IoT Greengrass deploys that group's deployment to the new device\.

You can define one deployment for each target\. When you create a new deployment for a target that has an existing deployment, you replace the previous deployment\. AWS IoT Greengrass applies the new deployment to the target devices\. 

You can only add, update, or delete up to 10 deployments at a time to a single target\.

Every deployment has a revision number that indicates how many deployment revisions you define for a target\. Use this operation to create a new revision of an existing deployment\. This operation returns the revision number of the new deployment when you create it\.

For more information, see the [Create deployments](https://docs.aws.amazon.com/greengrass/v2/developerguide/create-deployments.html) in the *AWS IoT Greengrass V2 Developer Guide*\.

**Important**  
Deployment resources are deleted when you delete stacks\. To keep the deployments in a stack, you must specify `"DeletionPolicy": "Retain"` on each deployment resource in the stack template that you want to keep\. For more information, see [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.  
You can only delete up to 10 deployment resources at a time\. If you delete more than 10 resources, you receive an error\.

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
The components to deploy\. This is a dictionary, where each key is the name of a component, and each key's value is the version and configuration to deploy for that component\.  
*Required*: No  
*Type*: Map of [ComponentDeploymentSpecification](aws-properties-greengrassv2-deployment-componentdeploymentspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentName`  <a name="cfn-greengrassv2-deployment-deploymentname"></a>
The name of the deployment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentPolicies`  <a name="cfn-greengrassv2-deployment-deploymentpolicies"></a>
The deployment policies for the deployment\. These policies define how the deployment updates components and handles failure\.  
*Required*: No  
*Type*: [DeploymentPolicies](aws-properties-greengrassv2-deployment-deploymentpolicies.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IotJobConfiguration`  <a name="cfn-greengrassv2-deployment-iotjobconfiguration"></a>
The job configuration for the deployment configuration\. The job configuration specifies the rollout, timeout, and stop configurations for the deployment configuration\.  
*Required*: No  
*Type*: [DeploymentIoTJobConfiguration](aws-properties-greengrassv2-deployment-deploymentiotjobconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-greengrassv2-deployment-tags"></a>
Application\-specific metadata to attach to the deployment\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tag your AWS IoT Greengrass Version 2 resources](https://docs.aws.amazon.com/greengrass/v2/developerguide/tag-resources.html) in the *AWS IoT Greengrass V2 Developer Guide*\.  
This `Json` property type is processed as a map of key\-value pairs\. It uses the following format, which is different from most `Tags` implementations in AWS CloudFormation templates\.  

```
"Tags": {
    "KeyName0": "value",
    "KeyName1": "value",
    "KeyName2": "value"
}
```
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-greengrassv2-deployment-targetarn"></a>
The ARN of the target AWS IoT thing or thing group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrassv2-deployment-return-values"></a>

### Ref<a name="aws-resource-greengrassv2-deployment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `DeploymentId`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrassv2-deployment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrassv2-deployment-return-values-fn--getatt-fn--getatt"></a>

`DeploymentId`  <a name="DeploymentId-fn::getatt"></a>
The ID of the deployment\.