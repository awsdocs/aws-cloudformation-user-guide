# AWS::Lex::Bot AudioAndDTMFInputSpecification<a name="aws-properties-lex-bot-audioanddtmfinputspecification"></a>

Specifies the audio and DTMF input specification\.

## Syntax<a name="aws-properties-lex-bot-audioanddtmfinputspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-audioanddtmfinputspecification-syntax.json"></a>

```
{
  "[AudioSpecification](#cfn-lex-bot-audioanddtmfinputspecification-audiospecification)" : AudioSpecification,
  "[DTMFSpecification](#cfn-lex-bot-audioanddtmfinputspecification-dtmfspecification)" : DTMFSpecification,
  "[StartTimeoutMs](#cfn-lex-bot-audioanddtmfinputspecification-starttimeoutms)" : Integer
}
```

### YAML<a name="aws-properties-lex-bot-audioanddtmfinputspecification-syntax.yaml"></a>

```
  [AudioSpecification](#cfn-lex-bot-audioanddtmfinputspecification-audiospecification): 
    AudioSpecification
  [DTMFSpecification](#cfn-lex-bot-audioanddtmfinputspecification-dtmfspecification): 
    DTMFSpecification
  [StartTimeoutMs](#cfn-lex-bot-audioanddtmfinputspecification-starttimeoutms): Integer
```

## Properties<a name="aws-properties-lex-bot-audioanddtmfinputspecification-properties"></a>

`AudioSpecification`  <a name="cfn-lex-bot-audioanddtmfinputspecification-audiospecification"></a>
Specifies the settings on audio input\.  
*Required*: No  
*Type*: [AudioSpecification](aws-properties-lex-bot-audiospecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DTMFSpecification`  <a name="cfn-lex-bot-audioanddtmfinputspecification-dtmfspecification"></a>
Specifies the settings on DTMF input\.  
*Required*: No  
*Type*: [DTMFSpecification](aws-properties-lex-bot-dtmfspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTimeoutMs`  <a name="cfn-lex-bot-audioanddtmfinputspecification-starttimeoutms"></a>
Time for which a bot waits before assuming that the customer isn't going to speak or press a key\. This timeout is shared between Audio and DTMF inputs\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)