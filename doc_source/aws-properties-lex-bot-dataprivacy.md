# AWS::Lex::Bot DataPrivacy<a name="aws-properties-lex-bot-dataprivacy"></a>

Provides information on additional privacy protections Amazon Lex should use with the bot's data\.

## Syntax<a name="aws-properties-lex-bot-dataprivacy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dataprivacy-syntax.json"></a>

```
{
  "[ChildDirected](#cfn-lex-bot-dataprivacy-childdirected)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-dataprivacy-syntax.yaml"></a>

```
  [ChildDirected](#cfn-lex-bot-dataprivacy-childdirected): Boolean
```

## Properties<a name="aws-properties-lex-bot-dataprivacy-properties"></a>

`ChildDirected`  <a name="cfn-lex-bot-dataprivacy-childdirected"></a>
For each Amazon Lex bot created with the Amazon Lex Model Building Service, you must specify whether your use of Amazon Lex is related to a website, program, or other application that is directed or targeted, in whole or in part, to children under age 13 and subject to the Children's Online Privacy Protection Act \(COPPA\) by specifying `true` or `false` in the `childDirected` field\. By specifying `true` in the `childDirected` field, you confirm that your use of Amazon Lex **is** related to a website, program, or other application that is directed or targeted, in whole or in part, to children under age 13 and subject to COPPA\. By specifying `false` in the `childDirected` field, you confirm that your use of Amazon Lex **is not** related to a website, program, or other application that is directed or targeted, in whole or in part, to children under age 13 and subject to COPPA\. You may not specify a default value for the `childDirected` field that does not accurately reflect whether your use of Amazon Lex is related to a website, program, or other application that is directed or targeted, in whole or in part, to children under age 13 and subject to COPPA\. If your use of Amazon Lex relates to a website, program, or other application that is directed in whole or in part, to children under age 13, you must obtain any required verifiable parental consent under COPPA\. For information regarding the use of Amazon Lex in connection with websites, programs, or other applications that are directed or targeted, in whole or in part, to children under age 13, see the [Amazon Lex FAQ](http://aws.amazon.com/lex/faqs#data-security)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)