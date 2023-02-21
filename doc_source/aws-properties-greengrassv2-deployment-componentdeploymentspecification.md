# AWS::GreengrassV2::Deployment ComponentDeploymentSpecification<a name="aws-properties-greengrassv2-deployment-componentdeploymentspecification"></a>

Contains information about a component to deploy\.

## Syntax<a name="aws-properties-greengrassv2-deployment-componentdeploymentspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-componentdeploymentspecification-syntax.json"></a>

```
{
  "[ComponentVersion](#cfn-greengrassv2-deployment-componentdeploymentspecification-componentversion)" : String,
  "[ConfigurationUpdate](#cfn-greengrassv2-deployment-componentdeploymentspecification-configurationupdate)" : ComponentConfigurationUpdate,
  "[RunWith](#cfn-greengrassv2-deployment-componentdeploymentspecification-runwith)" : ComponentRunWith
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-componentdeploymentspecification-syntax.yaml"></a>

```
  [ComponentVersion](#cfn-greengrassv2-deployment-componentdeploymentspecification-componentversion): String
  [ConfigurationUpdate](#cfn-greengrassv2-deployment-componentdeploymentspecification-configurationupdate): 
    ComponentConfigurationUpdate
  [RunWith](#cfn-greengrassv2-deployment-componentdeploymentspecification-runwith): 
    ComponentRunWith
```

## Properties<a name="aws-properties-greengrassv2-deployment-componentdeploymentspecification-properties"></a>

`ComponentVersion`  <a name="cfn-greengrassv2-deployment-componentdeploymentspecification-componentversion"></a>
The version of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationUpdate`  <a name="cfn-greengrassv2-deployment-componentdeploymentspecification-configurationupdate"></a>
The configuration updates to deploy for the component\. You can define reset updates and merge updates\. A reset updates the keys that you specify to the default configuration for the component\. A merge updates the core device's component configuration with the keys and values that you specify\. The AWS IoT Greengrass Core software applies reset updates before it applies merge updates\. For more information, see [Update component configuration](https://docs.aws.amazon.com/greengrass/v2/developerguide/update-component-configurations.html)\.  
*Required*: No  
*Type*: [ComponentConfigurationUpdate](aws-properties-greengrassv2-deployment-componentconfigurationupdate.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RunWith`  <a name="cfn-greengrassv2-deployment-componentdeploymentspecification-runwith"></a>
The system user and group that the software uses to run component processes on the core device\. If you omit this parameter, the software uses the system user and group that you configure for the core device\. For more information, see [Configure the user and group that run components](https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-greengrass-core-v2.html#configure-component-user) in the *AWS IoT Greengrass V2 Developer Guide*\.  
*Required*: No  
*Type*: [ComponentRunWith](aws-properties-greengrassv2-deployment-componentrunwith.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)