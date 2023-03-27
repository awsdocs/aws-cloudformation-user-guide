# AWS::Evidently::Launch<a name="aws-resource-evidently-launch"></a>

Creates or updates a *launch* of a given feature\. Before you create a launch, you must create the feature to use for the launch\.

You can use a launch to safely validate new features by serving them to a specified percentage of your users while you roll out the feature\. You can monitor the performance of the new feature to help you decide when to ramp up traffic to more users\. This helps you reduce risk and identify unintended consequences before you fully launch the feature\.

## Syntax<a name="aws-resource-evidently-launch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-evidently-launch-syntax.json"></a>

```
{
  "Type" : "AWS::Evidently::Launch",
  "Properties" : {
      "[Description](#cfn-evidently-launch-description)" : String,
      "[ExecutionStatus](#cfn-evidently-launch-executionstatus)" : ExecutionStatusObject,
      "[Groups](#cfn-evidently-launch-groups)" : [ LaunchGroupObject, ... ],
      "[MetricMonitors](#cfn-evidently-launch-metricmonitors)" : [ MetricDefinitionObject, ... ],
      "[Name](#cfn-evidently-launch-name)" : String,
      "[Project](#cfn-evidently-launch-project)" : String,
      "[RandomizationSalt](#cfn-evidently-launch-randomizationsalt)" : String,
      "[ScheduledSplitsConfig](#cfn-evidently-launch-scheduledsplitsconfig)" : [ StepConfig, ... ],
      "[Tags](#cfn-evidently-launch-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-evidently-launch-syntax.yaml"></a>

```
Type: AWS::Evidently::Launch
Properties: 
  [Description](#cfn-evidently-launch-description): String
  [ExecutionStatus](#cfn-evidently-launch-executionstatus): 
    ExecutionStatusObject
  [Groups](#cfn-evidently-launch-groups): 
    - LaunchGroupObject
  [MetricMonitors](#cfn-evidently-launch-metricmonitors): 
    - MetricDefinitionObject
  [Name](#cfn-evidently-launch-name): String
  [Project](#cfn-evidently-launch-project): String
  [RandomizationSalt](#cfn-evidently-launch-randomizationsalt): String
  [ScheduledSplitsConfig](#cfn-evidently-launch-scheduledsplitsconfig): 
    - StepConfig
  [Tags](#cfn-evidently-launch-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-evidently-launch-properties"></a>

`Description`  <a name="cfn-evidently-launch-description"></a>
An optional description for the launch\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionStatus`  <a name="cfn-evidently-launch-executionstatus"></a>
A structure that you can use to start and stop the launch\.  
*Required*: No  
*Type*: [ExecutionStatusObject](aws-properties-evidently-launch-executionstatusobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Groups`  <a name="cfn-evidently-launch-groups"></a>
An array of structures that contains the feature and variations that are to be used for the launch\. You can up to five launch groups in a launch\.  
*Required*: Yes  
*Type*: List of [LaunchGroupObject](aws-properties-evidently-launch-launchgroupobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricMonitors`  <a name="cfn-evidently-launch-metricmonitors"></a>
An array of structures that define the metrics that will be used to monitor the launch performance\. You can have up to three metric monitors in the array\.  
*Required*: No  
*Type*: List of [MetricDefinitionObject](aws-properties-evidently-launch-metricdefinitionobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-evidently-launch-name"></a>
The name for the launch\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Project`  <a name="cfn-evidently-launch-project"></a>
The name or ARN of the project that you want to create the launch in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RandomizationSalt`  <a name="cfn-evidently-launch-randomizationsalt"></a>
When Evidently assigns a particular user session to a launch, it must use a randomization ID to determine which variation the user session is served\. This randomization ID is a combination of the entity ID and `randomizationSalt`\. If you omit `randomizationSalt`, Evidently uses the launch name as the `randomizationsSalt`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledSplitsConfig`  <a name="cfn-evidently-launch-scheduledsplitsconfig"></a>
An array of structures that define the traffic allocation percentages among the feature variations during each step of the launch\.  
*Required*: Yes  
*Type*: List of [StepConfig](aws-properties-evidently-launch-stepconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-evidently-launch-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the launch\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with a launch\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-evidently-launch-return-values"></a>

### Ref<a name="aws-resource-evidently-launch-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the launch\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/launch/myLaunch`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-evidently-launch-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-evidently-launch-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the launch\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/launch/myLaunch`