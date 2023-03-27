# AWS::Cognito::UserPool DeviceConfiguration<a name="aws-properties-cognito-userpool-deviceconfiguration"></a>

The device\-remembering configuration for a user pool\. A [ DescribeUserPool](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_DescribeUserPool.html) request returns a null value for this object when the user pool isn't configured to remember devices\. When device remembering is active, you can remember a user's device with a [ConfirmDevice](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_ConfirmDevice.html) API request\. Additionally\. when the property `DeviceOnlyRememberedOnUserPrompt` is `true`, you must follow `ConfirmDevice` with an [UpdateDeviceStatus](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_UpdateDeviceStatus.html) API request that sets the user's device to `remembered` or `not_remembered`\.

To sign in with a remembered device, include `DEVICE_KEY` in the authentication parameters in your user's [ InitiateAuth](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_InitiateAuth.html) request\. If your app doesn't include a `DEVICE_KEY` parameter, the [response](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_InitiateAuth.html#API_InitiateAuth_ResponseSyntax) from Amazon Cognito includes newly\-generated `DEVICE_KEY` and `DEVICE_GROUP_KEY` values under `NewDeviceMetadata`\. Store these values to use in future device\-authentication requests\.

**Note**  
When you provide a value for any property of `DeviceConfiguration`, you activate the device remembering for the user pool\.

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
When true, a remembered device can sign in with device authentication instead of SMS and time\-based one\-time password \(TOTP\) factors for multi\-factor authentication \(MFA\)\.  
Whether or not `ChallengeRequiredOnNewDevice` is true, users who sign in with devices that have not been confirmed or remembered must still provide a second factor in a user pool that requires MFA\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceOnlyRememberedOnUserPrompt`  <a name="cfn-cognito-userpool-deviceconfiguration-deviceonlyrememberedonuserprompt"></a>
When true, Amazon Cognito doesn't automatically remember a user's device when your app sends a [ ConfirmDevice](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_ConfirmDevice.html) API request\. In your app, create a prompt for your user to choose whether they want to remember their device\. Return the user's choice in an [ UpdateDeviceStatus](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_UpdateDeviceStatus.html) API request\.  
When `DeviceOnlyRememberedOnUserPrompt` is `false`, Amazon Cognito immediately remembers devices that you register in a `ConfirmDevice` API request\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)