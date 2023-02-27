# AWS::Lex::BotAlias TextLogSetting<a name="aws-properties-lex-botalias-textlogsetting"></a>

Defines settings to enable text conversation logs\.

## Syntax<a name="aws-properties-lex-botalias-textlogsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-textlogsetting-syntax.json"></a>

```
{
  "[Destination](#cfn-lex-botalias-textlogsetting-destination)" : TextLogDestination,
  "[Enabled](#cfn-lex-botalias-textlogsetting-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-lex-botalias-textlogsetting-syntax.yaml"></a>

```
  [Destination](#cfn-lex-botalias-textlogsetting-destination): 
    TextLogDestination
  [Enabled](#cfn-lex-botalias-textlogsetting-enabled): Boolean
```

## Properties<a name="aws-properties-lex-botalias-textlogsetting-properties"></a>

`Destination`  <a name="cfn-lex-botalias-textlogsetting-destination"></a>
Defines the Amazon CloudWatch Logs destination log group for conversation text logs\.  
*Required*: Yes  
*Type*: [TextLogDestination](aws-properties-lex-botalias-textlogdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-lex-botalias-textlogsetting-enabled"></a>
Determines whether conversation logs should be stored for an alias\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)