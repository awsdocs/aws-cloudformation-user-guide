# AWS::Lex::BotAlias SentimentAnalysisSettings<a name="aws-properties-lex-botalias-sentimentanalysissettings"></a>

Determines whether Amazon Lex will use Amazon Comprehend to detect the sentiment of user utterances\.

## Syntax<a name="aws-properties-lex-botalias-sentimentanalysissettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-sentimentanalysissettings-syntax.json"></a>

```
{
  "[DetectSentiment](#cfn-lex-botalias-sentimentanalysissettings-detectsentiment)" : Boolean
}
```

### YAML<a name="aws-properties-lex-botalias-sentimentanalysissettings-syntax.yaml"></a>

```
  [DetectSentiment](#cfn-lex-botalias-sentimentanalysissettings-detectsentiment): Boolean
```

## Properties<a name="aws-properties-lex-botalias-sentimentanalysissettings-properties"></a>

`DetectSentiment`  <a name="cfn-lex-botalias-sentimentanalysissettings-detectsentiment"></a>
Sets whether Amazon Lex uses Amazon Comprehend to detect the sentiment of user utterances\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)