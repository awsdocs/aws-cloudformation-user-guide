# AWS::EMRServerless::Application AutoStartConfiguration<a name="aws-properties-emrserverless-application-autostartconfiguration"></a>

The conﬁguration for an application to automatically start on job submission\.

## Syntax<a name="aws-properties-emrserverless-application-autostartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-autostartconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-emrserverless-application-autostartconfiguration-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-emrserverless-application-autostartconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-emrserverless-application-autostartconfiguration-enabled): Boolean
```

## Properties<a name="aws-properties-emrserverless-application-autostartconfiguration-properties"></a>

`Enabled`  <a name="cfn-emrserverless-application-autostartconfiguration-enabled"></a>
Enables the application to automatically start on job submission\. Defaults to true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)