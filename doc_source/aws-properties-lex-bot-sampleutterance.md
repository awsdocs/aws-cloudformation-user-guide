# AWS::Lex::Bot SampleUtterance<a name="aws-properties-lex-bot-sampleutterance"></a>

A sample utterance that invokes and intent or responds to a slot elicitation prompt\.

## Syntax<a name="aws-properties-lex-bot-sampleutterance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-sampleutterance-syntax.json"></a>

```
{
  "[Utterance](#cfn-lex-bot-sampleutterance-utterance)" : String
}
```

### YAML<a name="aws-properties-lex-bot-sampleutterance-syntax.yaml"></a>

```
  [Utterance](#cfn-lex-bot-sampleutterance-utterance): String
```

## Properties<a name="aws-properties-lex-bot-sampleutterance-properties"></a>

`Utterance`  <a name="cfn-lex-bot-sampleutterance-utterance"></a>
The sample utterance that Amazon Lex uses to build its machine\-learning model to recognize intents\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)