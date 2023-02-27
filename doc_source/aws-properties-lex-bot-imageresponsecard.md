# AWS::Lex::Bot ImageResponseCard<a name="aws-properties-lex-bot-imageresponsecard"></a>

A card that is shown to the user by a messaging platform\. You define the contents of the card, the card is displayed by the platform\. 

When you use a response card, the response from the user is constrained to the text associated with a button on the card\.

## Syntax<a name="aws-properties-lex-bot-imageresponsecard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-imageresponsecard-syntax.json"></a>

```
{
  "[Buttons](#cfn-lex-bot-imageresponsecard-buttons)" : [ Button, ... ],
  "[ImageUrl](#cfn-lex-bot-imageresponsecard-imageurl)" : String,
  "[Subtitle](#cfn-lex-bot-imageresponsecard-subtitle)" : String,
  "[Title](#cfn-lex-bot-imageresponsecard-title)" : String
}
```

### YAML<a name="aws-properties-lex-bot-imageresponsecard-syntax.yaml"></a>

```
  [Buttons](#cfn-lex-bot-imageresponsecard-buttons): 
    - Button
  [ImageUrl](#cfn-lex-bot-imageresponsecard-imageurl): String
  [Subtitle](#cfn-lex-bot-imageresponsecard-subtitle): String
  [Title](#cfn-lex-bot-imageresponsecard-title): String
```

## Properties<a name="aws-properties-lex-bot-imageresponsecard-properties"></a>

`Buttons`  <a name="cfn-lex-bot-imageresponsecard-buttons"></a>
A list of buttons that should be displayed on the response card\. The arrangement of the buttons is determined by the platform that displays the button\.  
*Required*: No  
*Type*: List of [Button](aws-properties-lex-bot-button.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageUrl`  <a name="cfn-lex-bot-imageresponsecard-imageurl"></a>
The URL of an image to display on the response card\. The image URL must be publicly available so that the platform displaying the response card has access to the image\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtitle`  <a name="cfn-lex-bot-imageresponsecard-subtitle"></a>
The subtitle to display on the response card\. The format of the subtitle is determined by the platform displaying the response card\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-lex-bot-imageresponsecard-title"></a>
The title to display on the response card\. The format of the title is determined by the platform displaying the response card\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)