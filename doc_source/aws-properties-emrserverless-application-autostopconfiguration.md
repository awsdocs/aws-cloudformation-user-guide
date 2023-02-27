# AWS::EMRServerless::Application AutoStopConfiguration<a name="aws-properties-emrserverless-application-autostopconfiguration"></a>

The conﬁguration for an application to automatically stop after a certain amount of time being idle\.

## Syntax<a name="aws-properties-emrserverless-application-autostopconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-autostopconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-emrserverless-application-autostopconfiguration-enabled)" : Boolean,
  "[IdleTimeoutMinutes](#cfn-emrserverless-application-autostopconfiguration-idletimeoutminutes)" : Integer
}
```

### YAML<a name="aws-properties-emrserverless-application-autostopconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-emrserverless-application-autostopconfiguration-enabled): Boolean
  [IdleTimeoutMinutes](#cfn-emrserverless-application-autostopconfiguration-idletimeoutminutes): Integer
```

## Properties<a name="aws-properties-emrserverless-application-autostopconfiguration-properties"></a>

`Enabled`  <a name="cfn-emrserverless-application-autostopconfiguration-enabled"></a>
Enables the application to automatically stop after a certain amount of time being idle\. Defaults to true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdleTimeoutMinutes`  <a name="cfn-emrserverless-application-autostopconfiguration-idletimeoutminutes"></a>
The amount of idle time in minutes after which your application will automatically stop\. Defaults to 15 minutes\.  
*Minimum*: 1  
*Maximum*: 10080  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)