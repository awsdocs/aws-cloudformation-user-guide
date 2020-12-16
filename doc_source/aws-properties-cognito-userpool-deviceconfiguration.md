# AWS::Cognito::UserPool DeviceConfiguration<a name="aws-properties-cognito-userpool-deviceconfiguration"></a>

The configuration for the user pool's device tracking\.

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
Indicates whether a challenge is required on a new device\. Only applicable to a new device\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceOnlyRememberedOnUserPrompt`  <a name="cfn-cognito-userpool-deviceconfiguration-deviceonlyrememberedonuserprompt"></a>
If true, a device is only remembered on user prompt\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)