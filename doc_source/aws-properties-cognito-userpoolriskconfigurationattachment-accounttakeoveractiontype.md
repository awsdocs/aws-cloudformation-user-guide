# AWS::Cognito::UserPoolRiskConfigurationAttachment AccountTakeoverActionType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype"></a>

Account takeover action type\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-syntax.json"></a>

```
{
  "[EventAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-eventaction)" : String,
  "[Notify](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-notify)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-syntax.yaml"></a>

```
  [EventAction](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-eventaction): String
  [Notify](#cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-notify): Boolean
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-properties"></a>

`EventAction`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-eventaction"></a>
The event action\.  
+  `BLOCK` Choosing this action will block the request\.
+  `MFA_IF_CONFIGURED` Throw MFA challenge if user has configured it, else allow the request\.
+  `MFA_REQUIRED` Throw MFA challenge if user has configured it, else block the request\.
+  `NO_ACTION` Allow the user sign\-in\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `BLOCK | MFA_IF_CONFIGURED | MFA_REQUIRED | NO_ACTION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Notify`  <a name="cfn-cognito-userpoolriskconfigurationattachment-accounttakeoveractiontype-notify"></a>
Flag specifying whether to send a notification\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)