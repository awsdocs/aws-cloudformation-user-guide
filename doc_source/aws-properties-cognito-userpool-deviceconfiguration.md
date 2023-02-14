# AWS::Cognito::UserPool DeviceConfiguration<a name="aws-properties-cognito-userpool-deviceconfiguration"></a>

The device tracking configuration for a user pool\. A user pool with device tracking deactivated returns a null value\.

**Note**  
When you provide values for any DeviceConfiguration field, you activate device tracking\.

## Syntax<a name="aws-properties-cognito-userpool-deviceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-deviceconfiguration-syntax.json"></a>

```
{
  "[ChallengeRequiredOnNewDevice](#cfn-cognito-userpool-deviceconfiguration-challengerequiredonnewdevice)" : Boolean,
  "[DeviceOnlyRememberedOnUserPrompt](#cfn-cognito-userpool-deviceconfiguration-deviceonlyrememberedonuserprompt)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-deviceconfiguration-syntax.yaml"></a>

```
  [ChallengeRequiredOnNewDevice](#cfn-cognito-userpool-deviceconfiguration-challengerequiredonnewdevice): Boolean
  [DeviceOnlyRememberedOnUserPrompt](#cfn-cognito-userpool-deviceconfiguration-deviceonlyrememberedonuserprompt): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-deviceconfiguration-properties"></a>

`ChallengeRequiredOnNewDevice`  <a name="cfn-cognito-userpool-deviceconfiguration-challengerequiredonnewdevice"></a>
When true, device authentication can replace SMS and time\-based one\-time password \(TOTP\) factors for multi\-factor authentication \(MFA\)\.  
Users that sign in with devices that have not been confirmed or remembered will still have to provide a second factor, whether or not ChallengeRequiredOnNewDevice is true, when your user pool requires MFA\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceOnlyRememberedOnUserPrompt`  <a name="cfn-cognito-userpool-deviceconfiguration-deviceonlyrememberedonuserprompt"></a>
When true, users can opt in to remembering their device\. Your app code must use callback functions to return the user's choice\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)