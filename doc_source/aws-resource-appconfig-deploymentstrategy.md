# AWS::AppConfig::DeploymentStrategy<a name="aws-resource-appconfig-deploymentstrategy"></a>

The `AWS::AppConfig::DeploymentStrategy` resource creates an AppConfig deployment strategy\. A deployment strategy defines important criteria for rolling out your configuration to the designated targets\. A deployment strategy includes: the overall duration required, a percentage of targets to receive the deployment during each interval, an algorithm that defines how percentage grows, and bake time\.

AppConfig requires that you create resources and deploy a configuration in the following order:

1. Create an application

1. Create an environment

1. Create a configuration profile

1. Create a deployment strategy

1. Deploy the configuration

For more information, see [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) in the *AWS Systems Manager User Guide*\.

## Syntax<a name="aws-resource-appconfig-deploymentstrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-deploymentstrategy-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::DeploymentStrategy",
  "Properties" : {
      "[DeploymentDurationInMinutes](#cfn-appconfig-deploymentstrategy-deploymentdurationinminutes)" : Double,
      "[Description](#cfn-appconfig-deploymentstrategy-description)" : String,
      "[FinalBakeTimeInMinutes](#cfn-appconfig-deploymentstrategy-finalbaketimeinminutes)" : Double,
      "[GrowthFactor](#cfn-appconfig-deploymentstrategy-growthfactor)" : Double,
      "[GrowthType](#cfn-appconfig-deploymentstrategy-growthtype)" : String,
      "[Name](#cfn-appconfig-deploymentstrategy-name)" : String,
      "[ReplicateTo](#cfn-appconfig-deploymentstrategy-replicateto)" : String,
      "[Tags](#cfn-appconfig-deploymentstrategy-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-deploymentstrategy-syntax.yaml"></a>

```
Type: AWS::AppConfig::DeploymentStrategy
Properties: 
  [DeploymentDurationInMinutes](#cfn-appconfig-deploymentstrategy-deploymentdurationinminutes): Double
  [Description](#cfn-appconfig-deploymentstrategy-description): String
  [FinalBakeTimeInMinutes](#cfn-appconfig-deploymentstrategy-finalbaketimeinminutes): Double
  [GrowthFactor](#cfn-appconfig-deploymentstrategy-growthfactor): Double
  [GrowthType](#cfn-appconfig-deploymentstrategy-growthtype): String
  [Name](#cfn-appconfig-deploymentstrategy-name): String
  [ReplicateTo](#cfn-appconfig-deploymentstrategy-replicateto): String
  [Tags](#cfn-appconfig-deploymentstrategy-tags): 
    - Tags
```

## Properties<a name="aws-resource-appconfig-deploymentstrategy-properties"></a>

`DeploymentDurationInMinutes`  <a name="cfn-appconfig-deploymentstrategy-deploymentdurationinminutes"></a>
Total amount of time for a deployment to last\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `1440`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appconfig-deploymentstrategy-description"></a>
A description of the deployment strategy\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FinalBakeTimeInMinutes`  <a name="cfn-appconfig-deploymentstrategy-finalbaketimeinminutes"></a>
The amount of time AWS AppConfig monitors for alarms before considering the deployment to be complete and no longer eligible for automatic roll back\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `1440`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrowthFactor`  <a name="cfn-appconfig-deploymentstrategy-growthfactor"></a>
The percentage of targets to receive a deployed configuration during each interval\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrowthType`  <a name="cfn-appconfig-deploymentstrategy-growthtype"></a>
The algorithm used to define how percentage grows over time\. AWS AppConfig supports the following growth types:  
 **Linear**: For this type, AppConfig processes the deployment by dividing the total number of targets by the value specified for `Step percentage`\. For example, a linear deployment that uses a `Step percentage` of 10 deploys the configuration to 10 percent of the hosts\. After those deployments are complete, the system deploys the configuration to the next 10 percent\. This continues until 100% of the targets have successfully received the configuration\.  
 **Exponential**: For this type, AppConfig processes the deployment exponentially using the following formula: `G*(2^N)`\. In this formula, `G` is the growth factor specified by the user and `N` is the number of steps until the configuration is deployed to all targets\. For example, if you specify a growth factor of 2, then the system rolls out the configuration as follows:  
 `2*(2^0)`   
 `2*(2^1)`   
 `2*(2^2)`   
Expressed numerically, the deployment rolls out as follows: 2% of the targets, 4% of the targets, 8% of the targets, and continues until the configuration has been deployed to all targets\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EXPONENTIAL | LINEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appconfig-deploymentstrategy-name"></a>
A name for the deployment strategy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicateTo`  <a name="cfn-appconfig-deploymentstrategy-replicateto"></a>
Save the deployment strategy to a Systems Manager \(SSM\) document\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `NONE | SSM_DOCUMENT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appconfig-deploymentstrategy-tags"></a>
Metadata to assign to an AWS AppConfig resource\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\. You can specify a maximum of 50 tags for a resource\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-deploymentstrategy-tags.md) of [Tags](aws-properties-appconfig-deploymentstrategy-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appconfig-deploymentstrategy-return-values"></a>

### Ref<a name="aws-resource-appconfig-deploymentstrategy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the deployment strategy ID\.

## Examples<a name="aws-resource-appconfig-deploymentstrategy--examples"></a>



### AWS AppConfig Deployment Strategy Example<a name="aws-resource-appconfig-deploymentstrategy--examples--AWS_AppConfig_Deployment_Strategy_Example"></a>

The following example creates an AWS AppConfig deployment strategy called MyTestDeploymentStrategy\. A deployment strategy defines how a configuration is deployed\.

#### JSON<a name="aws-resource-appconfig-deploymentstrategy--examples--AWS_AppConfig_Deployment_Strategy_Example--json"></a>

```
Resources": {
    "BasicDeploymentStrategy": {
      "Type": "AWS::AppConfig::DeploymentStrategy",
      "Properties": {
        "Name": "MyTestDeploymentStrategy",
        "Description": "A sample test deployment strategy.",
        "DeploymentDurationInMinutes": 3,
        "FinalBakeTimeInMinutes": 4,
        "GrowthFactor": 10,
        "GrowthType": "LINEAR",
        "ReplicateTo": "NONE",
        "Tags": [
          {
            "Key": "Env",
            "Value": "test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-deploymentstrategy--examples--AWS_AppConfig_Deployment_Strategy_Example--yaml"></a>

```
Resources:
  BasicDeploymentStrategy:
    Type: AWS::AppConfig::DeploymentStrategy
    Properties:
      Name: "MyTestDeploymentStrategy"
      Description: "A sample test deployment strategy."
      DeploymentDurationInMinutes: 3
      FinalBakeTimeInMinutes: 4
      GrowthFactor: 10
      GrowthType: LINEAR
      ReplicateTo: NONE
      Tags:
        - Key: Env
          Value: test
```

## See also<a name="aws-resource-appconfig-deploymentstrategy--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) 
+  [Creating a deployment strategy](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-deployment-strategy.html)