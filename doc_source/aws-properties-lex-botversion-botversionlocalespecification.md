# AWS::Lex::BotVersion BotVersionLocaleSpecification<a name="aws-properties-lex-botversion-botversionlocalespecification"></a>

Specifies the locale that Amazon Lex adds to this version\. You can choose the Draft version or any other previously published version for each locale\. When you specify a source version, the locale data is copied from the source version to the new version\.

## Syntax<a name="aws-properties-lex-botversion-botversionlocalespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botversion-botversionlocalespecification-syntax.json"></a>

```
{
  "[BotVersionLocaleDetails](#cfn-lex-botversion-botversionlocalespecification-botversionlocaledetails)" : BotVersionLocaleDetails,
  "[LocaleId](#cfn-lex-botversion-botversionlocalespecification-localeid)" : String
}
```

### YAML<a name="aws-properties-lex-botversion-botversionlocalespecification-syntax.yaml"></a>

```
  [BotVersionLocaleDetails](#cfn-lex-botversion-botversionlocalespecification-botversionlocaledetails): 
    BotVersionLocaleDetails
  [LocaleId](#cfn-lex-botversion-botversionlocalespecification-localeid): String
```

## Properties<a name="aws-properties-lex-botversion-botversionlocalespecification-properties"></a>

`BotVersionLocaleDetails`  <a name="cfn-lex-botversion-botversionlocalespecification-botversionlocaledetails"></a>
The version of a bot used for a bot locale\.  
*Required*: Yes  
*Type*: [BotVersionLocaleDetails](aws-properties-lex-botversion-botversionlocaledetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleId`  <a name="cfn-lex-botversion-botversionlocalespecification-localeid"></a>
The identifier of the locale to add to the version\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)