# AWS::Lex::BotVersion BotVersionLocaleSpecificationItem<a name="aws-properties-lex-botversion-botversionlocalespecificationitem"></a>

Specifies the details of a locale in a bot version\.

## Syntax<a name="aws-properties-lex-botversion-botversionlocalespecificationitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botversion-botversionlocalespecificationitem-syntax.json"></a>

```
{
  "[BotVersionLocaleDetails](#cfn-lex-botversion-botversionlocalespecificationitem-botversionlocaledetails)" : BotVersionLocaleDetails,
  "[LocaleId](#cfn-lex-botversion-botversionlocalespecificationitem-localeid)" : String
}
```

### YAML<a name="aws-properties-lex-botversion-botversionlocalespecificationitem-syntax.yaml"></a>

```
  [BotVersionLocaleDetails](#cfn-lex-botversion-botversionlocalespecificationitem-botversionlocaledetails): 
    BotVersionLocaleDetails
  [LocaleId](#cfn-lex-botversion-botversionlocalespecificationitem-localeid): String
```

## Properties<a name="aws-properties-lex-botversion-botversionlocalespecificationitem-properties"></a>

`BotVersionLocaleDetails`  <a name="cfn-lex-botversion-botversionlocalespecificationitem-botversionlocaledetails"></a>
Information about the version of a bot used in a locale\.  
*Required*: Yes  
*Type*: [BotVersionLocaleDetails](aws-properties-lex-botversion-botversionlocaledetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleId`  <a name="cfn-lex-botversion-botversionlocalespecificationitem-localeid"></a>
The identifier of a specific bot locale\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)