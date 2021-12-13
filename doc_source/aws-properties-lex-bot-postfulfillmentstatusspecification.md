# AWS::Lex::Bot PostFulfillmentStatusSpecification<a name="aws-properties-lex-bot-postfulfillmentstatusspecification"></a>

Provides a setting that determines whether the post\-fulfillment response is sent to the user\. For more information, see [ Post\-fulfillment response ](https://docs.aws.amazon.com/latest/dg/streaming-progress.html#progress-complete) in the *Amazon Lex developer guide*\.

## Syntax<a name="aws-properties-lex-bot-postfulfillmentstatusspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-postfulfillmentstatusspecification-syntax.json"></a>

```
{
  "[FailureResponse](#cfn-lex-bot-postfulfillmentstatusspecification-failureresponse)" : ResponseSpecification,
  "[SuccessResponse](#cfn-lex-bot-postfulfillmentstatusspecification-successresponse)" : ResponseSpecification,
  "[TimeoutResponse](#cfn-lex-bot-postfulfillmentstatusspecification-timeoutresponse)" : ResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-postfulfillmentstatusspecification-syntax.yaml"></a>

```
  [FailureResponse](#cfn-lex-bot-postfulfillmentstatusspecification-failureresponse): 
    ResponseSpecification
  [SuccessResponse](#cfn-lex-bot-postfulfillmentstatusspecification-successresponse): 
    ResponseSpecification
  [TimeoutResponse](#cfn-lex-bot-postfulfillmentstatusspecification-timeoutresponse): 
    ResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-postfulfillmentstatusspecification-properties"></a>

`FailureResponse`  <a name="cfn-lex-bot-postfulfillmentstatusspecification-failureresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond when fulfillment isn't successful\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessResponse`  <a name="cfn-lex-bot-postfulfillmentstatusspecification-successresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond when the fulfillment is successful\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutResponse`  <a name="cfn-lex-bot-postfulfillmentstatusspecification-timeoutresponse"></a>
Specifies a list of message groups that Amazon Lex uses to respond when fulfillment isn't completed within the timeout period\.  
*Required*: No  
*Type*: [ResponseSpecification](aws-properties-lex-bot-responsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)