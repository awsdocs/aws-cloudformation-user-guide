# AWS::IoTAnalytics::Dataset LateDataRuleConfiguration<a name="aws-properties-iotanalytics-dataset-latedataruleconfiguration"></a>

The information needed to configure a delta time session window\.

## Syntax<a name="aws-properties-iotanalytics-dataset-latedataruleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-latedataruleconfiguration-syntax.json"></a>

```
{
  "[DeltaTimeSessionWindowConfiguration](#cfn-iotanalytics-dataset-latedataruleconfiguration-deltatimesessionwindowconfiguration)" : DeltaTimeSessionWindowConfiguration
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-latedataruleconfiguration-syntax.yaml"></a>

```
  [DeltaTimeSessionWindowConfiguration](#cfn-iotanalytics-dataset-latedataruleconfiguration-deltatimesessionwindowconfiguration): 
    DeltaTimeSessionWindowConfiguration
```

## Properties<a name="aws-properties-iotanalytics-dataset-latedataruleconfiguration-properties"></a>

`DeltaTimeSessionWindowConfiguration`  <a name="cfn-iotanalytics-dataset-latedataruleconfiguration-deltatimesessionwindowconfiguration"></a>
The information needed to configure a delta time session window\.  
*Required*: No  
*Type*: [DeltaTimeSessionWindowConfiguration](aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)