# AWS::IoTEvents::Input InputDefinition<a name="aws-properties-iotevents-input-inputdefinition"></a>

The definition of the input\.

## Syntax<a name="aws-properties-iotevents-input-inputdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-input-inputdefinition-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotevents-input-inputdefinition-attributes)" : [ [Attribute](aws-properties-iotevents-input-attribute.md), ... ]
}
```

### YAML<a name="aws-properties-iotevents-input-inputdefinition-syntax.yaml"></a>

```
  [Attributes](#cfn-iotevents-input-inputdefinition-attributes): 
    - [Attribute](aws-properties-iotevents-input-attribute.md)
```

## Properties<a name="aws-properties-iotevents-input-inputdefinition-properties"></a>

`Attributes`  <a name="cfn-iotevents-input-inputdefinition-attributes"></a>
The attributes from the JSON payload that are made available by the input\. Inputs are derived from messages sent to the AWS IoT Events system using `BatchPutMessage`\. Each such message contains a JSON payload, and those attributes \(and their paired values\) specified here are available for use in the `"condition"` expressions used by detectors that monitor this input\.   
*Required*: No  
*Type*: List of [Attribute](aws-properties-iotevents-input-attribute.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
