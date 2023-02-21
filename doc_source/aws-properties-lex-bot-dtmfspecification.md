# AWS::Lex::Bot DTMFSpecification<a name="aws-properties-lex-bot-dtmfspecification"></a>

Specifies the DTMF input specifications\.

## Syntax<a name="aws-properties-lex-bot-dtmfspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-dtmfspecification-syntax.json"></a>

```
{
  "[DeletionCharacter](#cfn-lex-bot-dtmfspecification-deletioncharacter)" : String,
  "[EndCharacter](#cfn-lex-bot-dtmfspecification-endcharacter)" : String,
  "[EndTimeoutMs](#cfn-lex-bot-dtmfspecification-endtimeoutms)" : Integer,
  "[MaxLength](#cfn-lex-bot-dtmfspecification-maxlength)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-dtmfspecification-syntax.yaml"></a>

```
  [DeletionCharacter](#cfn-lex-bot-dtmfspecification-deletioncharacter): String
  [EndCharacter](#cfn-lex-bot-dtmfspecification-endcharacter): String
  [EndTimeoutMs](#cfn-lex-bot-dtmfspecification-endtimeoutms): Integer
  [MaxLength](#cfn-lex-bot-dtmfspecification-maxlength): Integer
```

## Properties<a name="aws-properties-lex-bot-dtmfspecification-properties"></a>

`DeletionCharacter`  <a name="cfn-lex-bot-dtmfspecification-deletioncharacter"></a>
The DTMF character that clears the accumulated DTMF digits and immediately ends the input\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndCharacter`  <a name="cfn-lex-bot-dtmfspecification-endcharacter"></a>
The DTMF character that immediately ends input\. If the user does not press this character, the input ends after the end timeout\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndTimeoutMs`  <a name="cfn-lex-bot-dtmfspecification-endtimeoutms"></a>
How long the bot should wait after the last DTMF character input before assuming that the input has concluded\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLength`  <a name="cfn-lex-bot-dtmfspecification-maxlength"></a>
The maximum number of DTMF digits allowed in an utterance\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)