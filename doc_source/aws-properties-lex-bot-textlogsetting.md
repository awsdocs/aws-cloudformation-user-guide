# AWS::Lex::Bot TextLogSetting<a name="aws-properties-lex-bot-textlogsetting"></a>

Defines settings to enable text conversation logs\.

## Syntax<a name="aws-properties-lex-bot-textlogsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-textlogsetting-syntax.json"></a>

```
{
  "[Destination](#cfn-lex-bot-textlogsetting-destination)" : TextLogDestination,
  "[Enabled](#cfn-lex-bot-textlogsetting-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-textlogsetting-syntax.yaml"></a>

```
  [Destination](#cfn-lex-bot-textlogsetting-destination): 
    TextLogDestination
  [Enabled](#cfn-lex-bot-textlogsetting-enabled): Boolean
```

## Properties<a name="aws-properties-lex-bot-textlogsetting-properties"></a>

`Destination`  <a name="cfn-lex-bot-textlogsetting-destination"></a>
Specifies the Amazon CloudWatch Logs destination log group for conversation text logs\.  
*Required*: Yes  
*Type*: [TextLogDestination](aws-properties-lex-bot-textlogdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lex-bot-textlogsetting-enabled"></a>
Determines whether conversation logs should be stored for an alias\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)