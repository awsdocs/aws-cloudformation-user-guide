# AWS::Lex::Bot TextLogDestination<a name="aws-properties-lex-bot-textlogdestination"></a>

Defines the Amazon CloudWatch Logs destination log group for conversation text logs\.

## Syntax<a name="aws-properties-lex-bot-textlogdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-textlogdestination-syntax.json"></a>

```
{
  "[CloudWatch](#cfn-lex-bot-textlogdestination-cloudwatch)" : CloudWatchLogGroupLogDestination
}
```

### YAML<a name="aws-properties-lex-bot-textlogdestination-syntax.yaml"></a>

```
  [CloudWatch](#cfn-lex-bot-textlogdestination-cloudwatch): 
    CloudWatchLogGroupLogDestination
```

## Properties<a name="aws-properties-lex-bot-textlogdestination-properties"></a>

`CloudWatch`  <a name="cfn-lex-bot-textlogdestination-cloudwatch"></a>
Defines the Amazon CloudWatch Logs log group where text and metadata logs are delivered\.  
*Required*: Yes  
*Type*: [CloudWatchLogGroupLogDestination](aws-properties-lex-bot-cloudwatchloggrouplogdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)