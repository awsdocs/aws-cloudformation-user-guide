# AWS::Glue::Crawler Schedule<a name="aws-properties-glue-crawler-schedule"></a>

A scheduling object using a `cron` statement to schedule an event\.

## Syntax<a name="aws-properties-glue-crawler-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-schedule-syntax.json"></a>

```
{
  "[ScheduleExpression](#cfn-glue-crawler-schedule-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-schedule-syntax.yaml"></a>

```
  [ScheduleExpression](#cfn-glue-crawler-schedule-scheduleexpression): String
```

## Properties<a name="aws-properties-glue-crawler-schedule-properties"></a>

`ScheduleExpression`  <a name="cfn-glue-crawler-schedule-scheduleexpression"></a>
A `cron` expression used to specify the schedule\. For more information, see [Time\-Based Schedules for Jobs and Crawlers](https://docs.aws.amazon.com/glue/latest/dg/monitor-data-warehouse-schedule.html)\. For example, to run something every day at 12:15 UTC, specify `cron(15 12 * * ? *)`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)