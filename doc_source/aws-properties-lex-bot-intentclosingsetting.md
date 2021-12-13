# AWS::Lex::Bot IntentClosingSetting<a name="aws-properties-lex-bot-intentclosingsetting"></a>

Provides a statement the Amazon Lex conveys to the user when the intent is successfully fulfilled\.

## Syntax<a name="aws-properties-lex-bot-intentclosingsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-intentclosingsetting-syntax.json"></a>

```
{
  "[ClosingResponse](#cfn-lex-bot-intentclosingsetting-closingresponse)" : ResponseSpecification,
  "[IsActive](#cfn-lex-bot-intentclosingsetting-isactive)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-intentclosingsetting-syntax.yaml"></a>

```
  [ClosingResponse](#cfn-lex-bot-intentclosingsetting-closingresponse): 
    ResponseSpecification
  [IsActive](#cfn-lex-bot-intentclosingsetting-isactive): Boolean
```

## Properties<a name="aws-properties-lex-bot-intentclosingsetting-properties"></a>

`ClosingResponse`  <a name="cfn-lex-bot-intentclosingsetting-closingresponse"></a>
The response that Amazon Lex sends to the user when the intent is complete\.  
*Required*: Yes  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-intentclosingsetting-isactive"></a>
Specifies whether an intent's closing response is used\. When this field is false, the closing response isn't sent to the user and no closing input from the user is used\. If the IsActive field isn't specified, the default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)