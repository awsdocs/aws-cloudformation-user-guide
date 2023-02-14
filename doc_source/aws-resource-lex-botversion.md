# AWS::Lex::BotVersion<a name="aws-resource-lex-botversion"></a>

**Note**  
Amazon Lex V2 is the only supported version in AWS CloudFormation\.

Specifies a new version of the bot based on the `DRAFT` version\. If the `DRAFT` version of this resource hasn't changed since you created the last version, Amazon Lex doesn't create a new version, it returns the last created version\.

When you specify the first version of a bot, Amazon Lex sets the version to 1\. Subsequent versions increment by 1\.

## Syntax<a name="aws-resource-lex-botversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lex-botversion-syntax.json"></a>

```
{
  "Type" : "AWS::Lex::BotVersion",
  "Properties" : {
      "[BotId](#cfn-lex-botversion-botid)" : String,
      "[BotVersionLocaleSpecification](#cfn-lex-botversion-botversionlocalespecification)" : [ BotVersionLocaleSpecification, ... ],
      "[Description](#cfn-lex-botversion-description)" : String
    }
}
```

### YAML<a name="aws-resource-lex-botversion-syntax.yaml"></a>

```
Type: AWS::Lex::BotVersion
Properties: 
  [BotId](#cfn-lex-botversion-botid): String
  [BotVersionLocaleSpecification](#cfn-lex-botversion-botversionlocalespecification): 
    - BotVersionLocaleSpecification
  [Description](#cfn-lex-botversion-description): String
```

## Properties<a name="aws-resource-lex-botversion-properties"></a>

`BotId`  <a name="cfn-lex-botversion-botid"></a>
The unique identifier of the bot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BotVersionLocaleSpecification`  <a name="cfn-lex-botversion-botversionlocalespecification"></a>
Specifies the locales that Amazon Lex adds to this version\. You can choose the Draft version or any other previously published version for each locale\. When you specify a source version, the locale data is copied from the source version to the new version\.  
*Required*: Yes  
*Type*: [List](aws-properties-lex-botversion-botversionlocalespecification.md) of [BotVersionLocaleSpecification](aws-properties-lex-botversion-botversionlocalespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lex-botversion-description"></a>
The description of the version\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lex-botversion-return-values"></a>

### Fn::GetAtt<a name="aws-resource-lex-botversion-return-values-fn--getatt"></a>

#### <a name="aws-resource-lex-botversion-return-values-fn--getatt-fn--getatt"></a>

`BotVersion`  <a name="BotVersion-fn::getatt"></a>
The version of the bot\.