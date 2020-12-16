# AWS::KinesisAnalyticsV2::ApplicationOutput LambdaOutput<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput"></a>

When you configure a SQL\-based Kinesis Data Analytics application's output, identifies an AWS Lambda function as the destination\. You provide the function Amazon Resource Name \(ARN\) of the Lambda function\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-applicationoutput-lambdaoutput-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the destination Lambda function to write to\.  
To specify an earlier version of the Lambda function than the latest, include the Lambda function version in the Lambda function ARN\. For more information about Lambda ARNs, see [Example ARNs: AWS Lambda](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html#arn-syntax-lambda) 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationoutput-lambdaoutput--seealso"></a>
+  [LambdaOutput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_LambdaOutput.html) in the *Amazon Kinesis Data Analytics API Reference* 

