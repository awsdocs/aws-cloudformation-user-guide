# AWS::ImageBuilder::ImagePipeline Schedule<a name="aws-properties-imagebuilder-imagepipeline-schedule"></a>

A schedule configures how often and when a pipeline will automatically create a new image\. 

## Syntax<a name="aws-properties-imagebuilder-imagepipeline-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagepipeline-schedule-syntax.json"></a>

```
{
  "[PipelineExecutionStartCondition](#cfn-imagebuilder-imagepipeline-schedule-pipelineexecutionstartcondition)" : String,
  "[ScheduleExpression](#cfn-imagebuilder-imagepipeline-schedule-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-imagepipeline-schedule-syntax.yaml"></a>

```
  [PipelineExecutionStartCondition](#cfn-imagebuilder-imagepipeline-schedule-pipelineexecutionstartcondition): String
  [ScheduleExpression](#cfn-imagebuilder-imagepipeline-schedule-scheduleexpression): String
```

## Properties<a name="aws-properties-imagebuilder-imagepipeline-schedule-properties"></a>

`PipelineExecutionStartCondition`  <a name="cfn-imagebuilder-imagepipeline-schedule-pipelineexecutionstartcondition"></a>
The condition configures when the pipeline should trigger a new image build\. When the `pipelineExecutionStartCondition` is set to `EXPRESSION_MATCH_AND_DEPENDENCY_UPDATES_AVAILABLE`, and you use semantic version filters on the source image or components in your image recipe, EC2 Image Builder will build a new image only when there are new versions of the image or components in your recipe that match the semantic version filter\. When it is set to `EXPRESSION_MATCH_ONLY`, it will build a new image every time the CRON expression matches the current time\. For semantic version syntax, see [CreateComponent](https://docs.aws.amazon.com/imagebuilder/latest/APIReference/API_CreateComponent.html) in the * EC2 Image Builder API Reference*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EXPRESSION_MATCH_AND_DEPENDENCY_UPDATES_AVAILABLE | EXPRESSION_MATCH_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-imagebuilder-imagepipeline-schedule-scheduleexpression"></a>
The cron expression determines how often EC2 Image Builder evaluates your `pipelineExecutionStartCondition`\.   
For information on how to format a cron expression in Image Builder, see [Use cron expressions in EC2 Image Builder](https://docs.aws.amazon.com/imagebuilder/latest/userguide/image-builder-cron.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-imagebuilder-imagepipeline-schedule--seealso"></a>
+ [Create an image pipeline](https://docs.aws.amazon.com/imagebuilder/latest/userguide/managing-image-builder-cli.html#image-builder-cli-create-image-pipeline) in the *EC2 Image Builder User Guide*\.

