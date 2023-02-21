# AWS::Lex::Bot CloudWatchLogGroupLogDestination<a name="aws-properties-lex-bot-cloudwatchloggrouplogdestination"></a>

The Amazon CloudWatch Logs log group where the text and metadata logs are delivered\. The log group must exist before you enable logging\.

## Syntax<a name="aws-properties-lex-bot-cloudwatchloggrouplogdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-cloudwatchloggrouplogdestination-syntax.json"></a>

```
{
  "[CloudWatchLogGroupArn](#cfn-lex-bot-cloudwatchloggrouplogdestination-cloudwatchloggrouparn)" : String,
  "[LogPrefix](#cfn-lex-bot-cloudwatchloggrouplogdestination-logprefix)" : String
}
```

### YAML<a name="aws-properties-lex-bot-cloudwatchloggrouplogdestination-syntax.yaml"></a>

```
  [CloudWatchLogGroupArn](#cfn-lex-bot-cloudwatchloggrouplogdestination-cloudwatchloggrouparn): String
  [LogPrefix](#cfn-lex-bot-cloudwatchloggrouplogdestination-logprefix): String
```

## Properties<a name="aws-properties-lex-bot-cloudwatchloggrouplogdestination-properties"></a>

`CloudWatchLogGroupArn`  <a name="cfn-lex-bot-cloudwatchloggrouplogdestination-cloudwatchloggrouparn"></a>
The Amazon Resource Name \(ARN\) of the log group where text and metadata logs are delivered\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogPrefix`  <a name="cfn-lex-bot-cloudwatchloggrouplogdestination-logprefix"></a>
The prefix of the log stream name within the log group that you specified   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)