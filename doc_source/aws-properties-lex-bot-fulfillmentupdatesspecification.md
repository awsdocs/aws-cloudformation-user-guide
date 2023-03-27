# AWS::Lex::Bot FulfillmentUpdatesSpecification<a name="aws-properties-lex-bot-fulfillmentupdatesspecification"></a>

Provides information for updating the user on the progress of fulfilling an intent\.

## Syntax<a name="aws-properties-lex-bot-fulfillmentupdatesspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-fulfillmentupdatesspecification-syntax.json"></a>

```
{
  "[Active](#cfn-lex-bot-fulfillmentupdatesspecification-active)" : Boolean,
  "[StartResponse](#cfn-lex-bot-fulfillmentupdatesspecification-startresponse)" : FulfillmentStartResponseSpecification,
  "[TimeoutInSeconds](#cfn-lex-bot-fulfillmentupdatesspecification-timeoutinseconds)" : Integer,
  "[UpdateResponse](#cfn-lex-bot-fulfillmentupdatesspecification-updateresponse)" : FulfillmentUpdateResponseSpecification
}
```

### YAML<a name="aws-properties-lex-bot-fulfillmentupdatesspecification-syntax.yaml"></a>

```
  [Active](#cfn-lex-bot-fulfillmentupdatesspecification-active): Boolean
  [StartResponse](#cfn-lex-bot-fulfillmentupdatesspecification-startresponse): 
    FulfillmentStartResponseSpecification
  [TimeoutInSeconds](#cfn-lex-bot-fulfillmentupdatesspecification-timeoutinseconds): Integer
  [UpdateResponse](#cfn-lex-bot-fulfillmentupdatesspecification-updateresponse): 
    FulfillmentUpdateResponseSpecification
```

## Properties<a name="aws-properties-lex-bot-fulfillmentupdatesspecification-properties"></a>

`Active`  <a name="cfn-lex-bot-fulfillmentupdatesspecification-active"></a>
Determines whether fulfillment updates are sent to the user\. When this field is true, updates are sent\.  
If the `active` field is set to true, the `startResponse`, `updateResponse`, and `timeoutInSeconds` fields are required\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartResponse`  <a name="cfn-lex-bot-fulfillmentupdatesspecification-startresponse"></a>
Provides configuration information for the message sent to users when the fulfillment Lambda functions starts running\.  
*Required*: No  
*Type*: [FulfillmentStartResponseSpecification](aws-properties-lex-bot-fulfillmentstartresponsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInSeconds`  <a name="cfn-lex-bot-fulfillmentupdatesspecification-timeoutinseconds"></a>
The length of time that the fulfillment Lambda function should run before it times out\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateResponse`  <a name="cfn-lex-bot-fulfillmentupdatesspecification-updateresponse"></a>
Provides configuration information for messages sent periodically to the user while the fulfillment Lambda function is running\.  
*Required*: No  
*Type*: [FulfillmentUpdateResponseSpecification](aws-properties-lex-bot-fulfillmentupdateresponsespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)