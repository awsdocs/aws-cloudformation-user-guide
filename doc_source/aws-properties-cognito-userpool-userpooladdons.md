# AWS::Cognito::UserPool UserPoolAddOns<a name="aws-properties-cognito-userpool-userpooladdons"></a>

User pool add\-ons\. Contains settings for activation of advanced security features\. To log user security information but take no action, set to `AUDIT`\. To configure automatic security responses to risky traffic to your user pool, set to `ENFORCED`\.

For more information, see [Adding advanced security to a user pool](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pool-settings-advanced-security.html)\.

## Syntax<a name="aws-properties-cognito-userpool-userpooladdons-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-userpooladdons-syntax.json"></a>

```
{
  "[AdvancedSecurityMode](#cfn-cognito-userpool-userpooladdons-advancedsecuritymode)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-userpooladdons-syntax.yaml"></a>

```
  [AdvancedSecurityMode](#cfn-cognito-userpool-userpooladdons-advancedsecuritymode): String
```

## Properties<a name="aws-properties-cognito-userpool-userpooladdons-properties"></a>

`AdvancedSecurityMode`  <a name="cfn-cognito-userpool-userpooladdons-advancedsecuritymode"></a>
The operating mode of advanced security features in your user pool\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUDIT | ENFORCED | OFF`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)