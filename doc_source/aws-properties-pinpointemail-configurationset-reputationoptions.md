# AWS::PinpointEmail::ConfigurationSet ReputationOptions<a name="aws-properties-pinpointemail-configurationset-reputationoptions"></a>

Enable or disable collection of reputation metrics for emails that you send using this configuration set in the current AWS Region\. 

## Syntax<a name="aws-properties-pinpointemail-configurationset-reputationoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationset-reputationoptions-syntax.json"></a>

```
{
  "[ReputationMetricsEnabled](#cfn-pinpointemail-configurationset-reputationoptions-reputationmetricsenabled)" : Boolean
}
```

### YAML<a name="aws-properties-pinpointemail-configurationset-reputationoptions-syntax.yaml"></a>

```
  [ReputationMetricsEnabled](#cfn-pinpointemail-configurationset-reputationoptions-reputationmetricsenabled): Boolean
```

## Properties<a name="aws-properties-pinpointemail-configurationset-reputationoptions-properties"></a>

`ReputationMetricsEnabled`  <a name="cfn-pinpointemail-configurationset-reputationoptions-reputationmetricsenabled"></a>
If `true`, tracking of reputation metrics is enabled for the configuration set\. If `false`, tracking of reputation metrics is disabled for the configuration set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)