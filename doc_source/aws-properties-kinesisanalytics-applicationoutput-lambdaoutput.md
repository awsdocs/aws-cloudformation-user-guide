# AWS::KinesisAnalytics::ApplicationOutput LambdaOutput<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput"></a>

When configuring application output, identifies an AWS Lambda function as the destination\. You provide the function Amazon Resource Name \(ARN\) and also an IAM role ARN that Amazon Kinesis Analytics can use to write to the function on your behalf\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn)" : String,
  "[RoleARN](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn): String
  [RoleARN](#cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationoutput-lambdaoutput-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalytics-applicationoutput-lambdaoutput-resourcearn"></a>
Amazon Resource Name \(ARN\) of the destination Lambda function to write to\.  
To specify an earlier version of the Lambda function than the latest, include the Lambda function version in the Lambda function ARN\. For more information about Lambda ARNs, see [Example ARNs: AWS Lambda](/general/latest/gr/aws-arns-and-namespaces.html#arn-syntax-lambda) 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-kinesisanalytics-applicationoutput-lambdaoutput-rolearn"></a>
ARN of the IAM role that Amazon Kinesis Analytics can assume to write to the destination function on your behalf\. You need to grant the necessary permissions to this role\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:aws:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
