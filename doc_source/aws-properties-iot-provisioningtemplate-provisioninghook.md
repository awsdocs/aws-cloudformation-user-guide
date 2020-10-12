# AWS::IoT::ProvisioningTemplate ProvisioningHook<a name="aws-properties-iot-provisioningtemplate-provisioninghook"></a>

Structure that contains payloadVersion and targetArn\. Provisioning hooks can be used when fleet provisioning to validate device parameters before allowing the device to be provisioned\.

## Syntax<a name="aws-properties-iot-provisioningtemplate-provisioninghook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-provisioningtemplate-provisioninghook-syntax.json"></a>

```
{
  "[PayloadVersion](#cfn-iot-provisioningtemplate-provisioninghook-payloadversion)" : String,
  "[TargetArn](#cfn-iot-provisioningtemplate-provisioninghook-targetarn)" : String
}
```

### YAML<a name="aws-properties-iot-provisioningtemplate-provisioninghook-syntax.yaml"></a>

```
  [PayloadVersion](#cfn-iot-provisioningtemplate-provisioninghook-payloadversion): String
  [TargetArn](#cfn-iot-provisioningtemplate-provisioninghook-targetarn): String
```

## Properties<a name="aws-properties-iot-provisioningtemplate-provisioninghook-properties"></a>

`PayloadVersion`  <a name="cfn-iot-provisioningtemplate-provisioninghook-payloadversion"></a>
The payload that was sent to the target function\. The valid payload is `"2020-04-01"`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iot-provisioningtemplate-provisioninghook-targetarn"></a>
The ARN of the target function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)