# AWS::IoTEvents::DetectorModel SetVariable<a name="aws-properties-iotevents-detectormodel-setvariable"></a>

Information about the variable and its new value\.

## Syntax<a name="aws-properties-iotevents-detectormodel-setvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-setvariable-syntax.json"></a>

```
{
  "[Value](#cfn-iotevents-detectormodel-setvariable-value)" : String,
  "[VariableName](#cfn-iotevents-detectormodel-setvariable-variablename)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-setvariable-syntax.yaml"></a>

```
  [Value](#cfn-iotevents-detectormodel-setvariable-value): String
  [VariableName](#cfn-iotevents-detectormodel-setvariable-variablename): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-setvariable-properties"></a>

`Value`  <a name="cfn-iotevents-detectormodel-setvariable-value"></a>
The new value of the variable\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariableName`  <a name="cfn-iotevents-detectormodel-setvariable-variablename"></a>
The name of the variable\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)