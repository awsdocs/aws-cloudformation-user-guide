# AWS::DataBrew::Schedule<a name="aws-resource-databrew-schedule"></a>

Creates a new schedule for one or more DataBrew jobs\. Jobs can be run at a specific date and time, or at regular intervals\.

## Syntax<a name="aws-resource-databrew-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-schedule-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Schedule",
  "Properties" : {
      "[CronExpression](#cfn-databrew-schedule-cronexpression)" : String,
      "[JobNames](#cfn-databrew-schedule-jobnames)" : [ String, ... ],
      "[Name](#cfn-databrew-schedule-name)" : String,
      "[Tags](#cfn-databrew-schedule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-databrew-schedule-syntax.yaml"></a>

```
Type: AWS::DataBrew::Schedule
Properties: 
  [CronExpression](#cfn-databrew-schedule-cronexpression): String
  [JobNames](#cfn-databrew-schedule-jobnames): 
    - String
  [Name](#cfn-databrew-schedule-name): String
  [Tags](#cfn-databrew-schedule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-databrew-schedule-properties"></a>

`CronExpression`  <a name="cfn-databrew-schedule-cronexpression"></a>
The date\(s\) and time\(s\) when the job will run\. For more information, see [Cron expressions](https://docs.aws.amazon.com/databrew/latest/dg/jobs.cron.html) in the *AWS Glue DataBrew Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobNames`  <a name="cfn-databrew-schedule-jobnames"></a>
A list of jobs to be run, according to the schedule\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-schedule-name"></a>
The name of the schedule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-databrew-schedule-tags"></a>
Metadata tags that have been applied to the schedule\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-databrew-schedule-return-values"></a>

### Ref<a name="aws-resource-databrew-schedule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myDataset" }` 

For the AWS Glue DataBrew dataset `myDataset`, `Ref` returns the name of the dataset\.