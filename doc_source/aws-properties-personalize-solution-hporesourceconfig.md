# AWS::Personalize::Solution HpoResourceConfig<a name="aws-properties-personalize-solution-hporesourceconfig"></a>

Describes the resource configuration for hyperparameter optimization \(HPO\)\.

## Syntax<a name="aws-properties-personalize-solution-hporesourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-personalize-solution-hporesourceconfig-syntax.json"></a>

```
{
  "[MaxNumberOfTrainingJobs](#cfn-personalize-solution-hporesourceconfig-maxnumberoftrainingjobs)" : String,
  "[MaxParallelTrainingJobs](#cfn-personalize-solution-hporesourceconfig-maxparalleltrainingjobs)" : String
}
```

### YAML<a name="aws-properties-personalize-solution-hporesourceconfig-syntax.yaml"></a>

```
  [MaxNumberOfTrainingJobs](#cfn-personalize-solution-hporesourceconfig-maxnumberoftrainingjobs): String
  [MaxParallelTrainingJobs](#cfn-personalize-solution-hporesourceconfig-maxparalleltrainingjobs): String
```

## Properties<a name="aws-properties-personalize-solution-hporesourceconfig-properties"></a>

`MaxNumberOfTrainingJobs`  <a name="cfn-personalize-solution-hporesourceconfig-maxnumberoftrainingjobs"></a>
The maximum number of training jobs when you create a solution version\. The maximum value for `maxNumberOfTrainingJobs` is `40`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxParallelTrainingJobs`  <a name="cfn-personalize-solution-hporesourceconfig-maxparalleltrainingjobs"></a>
The maximum number of parallel training jobs when you create a solution version\. The maximum value for `maxParallelTrainingJobs` is `10`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)