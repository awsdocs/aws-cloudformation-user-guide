# AWS::LookoutMetrics::Alert SNSConfiguration<a name="aws-properties-lookoutmetrics-alert-snsconfiguration"></a>

Contains information about the SNS topic to which you want to send your alerts and the IAM role that has access to that topic\.

## Syntax<a name="aws-properties-lookoutmetrics-alert-snsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-alert-snsconfiguration-syntax.json"></a>

```
{
  "[RoleArn](#cfn-lookoutmetrics-alert-snsconfiguration-rolearn)" : String,
  "[SnsTopicArn](#cfn-lookoutmetrics-alert-snsconfiguration-snstopicarn)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-alert-snsconfiguration-syntax.yaml"></a>

```
  [RoleArn](#cfn-lookoutmetrics-alert-snsconfiguration-rolearn): String
  [SnsTopicArn](#cfn-lookoutmetrics-alert-snsconfiguration-snstopicarn): String
```

## Properties<a name="aws-properties-lookoutmetrics-alert-snsconfiguration-properties"></a>

`RoleArn`  <a name="cfn-lookoutmetrics-alert-snsconfiguration-rolearn"></a>
The ARN of the IAM role that has access to the target SNS topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnsTopicArn`  <a name="cfn-lookoutmetrics-alert-snsconfiguration-snstopicarn"></a>
The ARN of the target SNS topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)