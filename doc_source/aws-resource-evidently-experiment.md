# AWS::Evidently::Experiment<a name="aws-resource-evidently-experiment"></a>

Creates or updates an Evidently *experiment*\. Before you create an experiment, you must create the feature to use for the experiment\.

An experiment helps you make feature design decisions based on evidence and data\. An experiment can test as many as five variations at once\. Evidently collects experiment data and analyzes it by statistical methods, and provides clear recommendations about which variations perform better\.

## Syntax<a name="aws-resource-evidently-experiment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-evidently-experiment-syntax.json"></a>

```
{
  "Type" : "AWS::Evidently::Experiment",
  "Properties" : {
      "[Description](#cfn-evidently-experiment-description)" : String,
      "[MetricGoals](#cfn-evidently-experiment-metricgoals)" : [ MetricGoalObject, ... ],
      "[Name](#cfn-evidently-experiment-name)" : String,
      "[OnlineAbConfig](#cfn-evidently-experiment-onlineabconfig)" : OnlineAbConfigObject,
      "[Project](#cfn-evidently-experiment-project)" : String,
      "[RandomizationSalt](#cfn-evidently-experiment-randomizationsalt)" : String,
      "[RemoveSegment](#cfn-evidently-experiment-removesegment)" : Boolean,
      "[RunningStatus](#cfn-evidently-experiment-runningstatus)" : RunningStatusObject,
      "[SamplingRate](#cfn-evidently-experiment-samplingrate)" : Integer,
      "[Segment](#cfn-evidently-experiment-segment)" : String,
      "[Tags](#cfn-evidently-experiment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Treatments](#cfn-evidently-experiment-treatments)" : [ TreatmentObject, ... ]
    }
}
```

### YAML<a name="aws-resource-evidently-experiment-syntax.yaml"></a>

```
Type: AWS::Evidently::Experiment
Properties: 
  [Description](#cfn-evidently-experiment-description): String
  [MetricGoals](#cfn-evidently-experiment-metricgoals): 
    - MetricGoalObject
  [Name](#cfn-evidently-experiment-name): String
  [OnlineAbConfig](#cfn-evidently-experiment-onlineabconfig): 
    OnlineAbConfigObject
  [Project](#cfn-evidently-experiment-project): String
  [RandomizationSalt](#cfn-evidently-experiment-randomizationsalt): String
  [RemoveSegment](#cfn-evidently-experiment-removesegment): Boolean
  [RunningStatus](#cfn-evidently-experiment-runningstatus): 
    RunningStatusObject
  [SamplingRate](#cfn-evidently-experiment-samplingrate): Integer
  [Segment](#cfn-evidently-experiment-segment): String
  [Tags](#cfn-evidently-experiment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Treatments](#cfn-evidently-experiment-treatments): 
    - TreatmentObject
```

## Properties<a name="aws-resource-evidently-experiment-properties"></a>

`Description`  <a name="cfn-evidently-experiment-description"></a>
An optional description of the experiment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricGoals`  <a name="cfn-evidently-experiment-metricgoals"></a>
An array of structures that defines the metrics used for the experiment, and whether a higher or lower value for each metric is the goal\. You can use up to three metrics in an experiment\.  
*Required*: Yes  
*Type*: List of [MetricGoalObject](aws-properties-evidently-experiment-metricgoalobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-evidently-experiment-name"></a>
A name for the new experiment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OnlineAbConfig`  <a name="cfn-evidently-experiment-onlineabconfig"></a>
A structure that contains the configuration of which variation to use as the "control" version\. The "control" version is used for comparison with other variations\. This structure also specifies how much experiment traffic is allocated to each variation\.  
*Required*: Yes  
*Type*: [OnlineAbConfigObject](aws-properties-evidently-experiment-onlineabconfigobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Project`  <a name="cfn-evidently-experiment-project"></a>
The name or the ARN of the project where this experiment is to be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RandomizationSalt`  <a name="cfn-evidently-experiment-randomizationsalt"></a>
When Evidently assigns a particular user session to an experiment, it must use a randomization ID to determine which variation the user session is served\. This randomization ID is a combination of the entity ID and `randomizationSalt`\. If you omit `randomizationSalt`, Evidently uses the experiment name as the `randomizationSalt`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveSegment`  <a name="cfn-evidently-experiment-removesegment"></a>
Set this to `true` to remove the segment that is associated with this experiment\. You can't use this parameter if the experiment is currently running\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunningStatus`  <a name="cfn-evidently-experiment-runningstatus"></a>
A structure that you can use to start and stop the experiment\.  
*Required*: No  
*Type*: [RunningStatusObject](aws-properties-evidently-experiment-runningstatusobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplingRate`  <a name="cfn-evidently-experiment-samplingrate"></a>
The portion of the available audience that you want to allocate to this experiment, in thousandths of a percent\. The available audience is the total audience minus the audience that you have allocated to overrides or current launches of this feature\.  
This is represented in thousandths of a percent\. For example, specify 10,000 to allocate 10% of the available audience\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Segment`  <a name="cfn-evidently-experiment-segment"></a>
Specifies an audience *segment* to use in the experiment\. When a segment is used in an experiment, only user sessions that match the segment pattern are used in the experiment\.  
For more information, see [ Segment rule pattern syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments-syntax.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-evidently-experiment-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the experiment\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with an experiment\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Treatments`  <a name="cfn-evidently-experiment-treatments"></a>
An array of structures that describe the configuration of each feature variation used in the experiment\.  
*Required*: Yes  
*Type*: List of [TreatmentObject](aws-properties-evidently-experiment-treatmentobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-evidently-experiment-return-values"></a>

### Ref<a name="aws-resource-evidently-experiment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the experiment\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/experiment/myExperiment` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-evidently-experiment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-evidently-experiment-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the experiment\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject/experiment/myExperiment`