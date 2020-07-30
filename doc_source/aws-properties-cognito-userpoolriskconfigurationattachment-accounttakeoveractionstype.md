# AWS::Cognito::UserPoolRiskConfigurationAttachment AccountTakeoverActionsType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype"></a>

Account takeover actions type\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-syntax.json"></a>

```
{
  "[HighAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-highaction)" : AccountTakeoverActionType,
  "[LowAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-lowaction)" : AccountTakeoverActionType,
  "[MediumAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-mediumaction)" : AccountTakeoverActionType
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-syntax.yaml"></a>

```
  [HighAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-highaction): 
    AccountTakeoverActionType
  [LowAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-lowaction): 
    AccountTakeoverActionType
  [MediumAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-mediumaction): 
    AccountTakeoverActionType
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-properties"></a>

`HighAction`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-highaction"></a>
Action to take for a high risk\.  
*Required*: No  
*Type*: [AccountTakeoverActionType](aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LowAction`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-lowaction"></a>
Action to take for a low risk\.  
*Required*: No  
*Type*: [AccountTakeoverActionType](aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediumAction`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractionstype-mediumaction"></a>
Action to take for a medium risk\.  
*Required*: No  
*Type*: [AccountTakeoverActionType](aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)