# AWS::KinesisAnalytics::Application InputParallelism<a name="aws-properties-kinesisanalytics-application-inputparallelism"></a>

Describes the number of in\-application streams to create for a given streaming source\. For information about parallelism, see [Configuring Application Input](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-input.html)\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax.json"></a>

```
{
  "[Count](#cfn-kinesisanalytics-application-inputparallelism-count)" : Integer
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputparallelism-syntax.yaml"></a>

```
  [Count](#cfn-kinesisanalytics-application-inputparallelism-count): Integer
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputparallelism-properties"></a>

`Count`  <a name="cfn-kinesisanalytics-application-inputparallelism-count"></a>
Number of in\-application streams to create\. For more information, see [Limits](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/limits.html)\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)