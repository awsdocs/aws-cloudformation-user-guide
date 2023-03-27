# AWS::Lex::BotAlias TextLogDestination<a name="aws-properties-lex-botalias-textlogdestination"></a>

Defines the Amazon CloudWatch Logs destination log group for conversation text logs\.

## Syntax<a name="aws-properties-lex-botalias-textlogdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-textlogdestination-syntax.json"></a>

```
{
  "[CloudWatch](#cfn-lex-botalias-textlogdestination-cloudwatch)" : CloudWatchLogGroupLogDestination
}
```

### YAML<a name="aws-properties-lex-botalias-textlogdestination-syntax.yaml"></a>

```
  [CloudWatch](#cfn-lex-botalias-textlogdestination-cloudwatch): 
    CloudWatchLogGroupLogDestination
```

## Properties<a name="aws-properties-lex-botalias-textlogdestination-properties"></a>

`CloudWatch`  <a name="cfn-lex-botalias-textlogdestination-cloudwatch"></a>
Defines the Amazon CloudWatch Logs log group where text and metadata logs are delivered\.  
*Required*: Yes  
*Type*: [CloudWatchLogGroupLogDestination](aws-properties-lex-botalias-cloudwatchloggrouplogdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)