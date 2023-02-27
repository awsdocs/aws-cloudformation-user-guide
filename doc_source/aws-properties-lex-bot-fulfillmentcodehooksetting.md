# AWS::Lex::Bot FulfillmentCodeHookSetting<a name="aws-properties-lex-bot-fulfillmentcodehooksetting"></a>

Determines if a Lambda function should be invoked for a specific intent\.

## Syntax<a name="aws-properties-lex-bot-fulfillmentcodehooksetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-fulfillmentcodehooksetting-syntax.json"></a>

```
{
  "[Enabled](#cfn-lex-bot-fulfillmentcodehooksetting-enabled)" : Boolean,
  "[FulfillmentUpdatesSpecification](#cfn-lex-bot-fulfillmentcodehooksetting-fulfillmentupdatesspecification)" : FulfillmentUpdatesSpecification,
  "[IsActive](#cfn-lex-bot-fulfillmentcodehooksetting-isactive)" : Boolean,
  "[PostFulfillmentStatusSpecification](#cfn-lex-bot-fulfillmentcodehooksetting-postfulfillmentstatusspecification)" : PostFulfillmentStatusSpecification
}
```

### YAML<a name="aws-properties-lex-bot-fulfillmentcodehooksetting-syntax.yaml"></a>

```
  [Enabled](#cfn-lex-bot-fulfillmentcodehooksetting-enabled): Boolean
  [FulfillmentUpdatesSpecification](#cfn-lex-bot-fulfillmentcodehooksetting-fulfillmentupdatesspecification): 
    FulfillmentUpdatesSpecification
  [IsActive](#cfn-lex-bot-fulfillmentcodehooksetting-isactive): Boolean
  [PostFulfillmentStatusSpecification](#cfn-lex-bot-fulfillmentcodehooksetting-postfulfillmentstatusspecification): 
    PostFulfillmentStatusSpecification
```

## Properties<a name="aws-properties-lex-bot-fulfillmentcodehooksetting-properties"></a>

`Enabled`  <a name="cfn-lex-bot-fulfillmentcodehooksetting-enabled"></a>
Indicates whether a Lambda function should be invoked to fulfill a specific intent\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FulfillmentUpdatesSpecification`  <a name="cfn-lex-bot-fulfillmentcodehooksetting-fulfillmentupdatesspecification"></a>
Provides settings for update messages sent to the user for long\-running Lambda fulfillment functions\. Fulfillment updates can be used only with streaming conversations\.  
*Required*: No  
*Type*: [FulfillmentUpdatesSpecification](aws-properties-lex-bot-fulfillmentupdatesspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsActive`  <a name="cfn-lex-bot-fulfillmentcodehooksetting-isactive"></a>
Determines whether the fulfillment code hook is used\. When `active` is false, the code hook doesn't run\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostFulfillmentStatusSpecification`  <a name="cfn-lex-bot-fulfillmentcodehooksetting-postfulfillmentstatusspecification"></a>
Provides settings for messages sent to the user for after the Lambda fulfillment function completes\. Post\-fulfillment messages can be sent for both streaming and non\-streaming conversations\.  
*Required*: No  
*Type*: [PostFulfillmentStatusSpecification](aws-properties-lex-bot-postfulfillmentstatusspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)