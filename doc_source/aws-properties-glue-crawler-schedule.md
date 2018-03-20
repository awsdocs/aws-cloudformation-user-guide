# AWS Glue Crawler Schedule<a name="aws-properties-glue-crawler-schedule"></a>

<a name="aws-properties-glue-crawler-schedule-description"></a>The `Schedule` property type schedules an event for an AWS Glue crawler using a `cron` statement\.

<a name="aws-properties-glue-crawler-schedule-inheritance"></a> `Schedule` is a property of the [AWS::Glue::Crawler](aws-resource-glue-crawler.md) resource\.

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

For more information, see [Schedule Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-Schedule) in the *AWS Glue Developer Guide*\.

`ScheduleExpression`  <a name="cfn-glue-crawler-schedule-scheduleexpression"></a>
A `cron` expression that you can use as an Amazon CloudWatch Events event to schedule something\. For example, to run something every day at 12:15 UTC, you would specify: `cron(15 12 * * ? *)`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 