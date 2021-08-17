# AWS::IoT::MitigationAction ActionParams<a name="aws-properties-iot-mitigationaction-actionparams"></a>

Defines the type of action and the parameters for that action\.

## Syntax<a name="aws-properties-iot-mitigationaction-actionparams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-mitigationaction-actionparams-syntax.json"></a>

```
{
  "[AddThingsToThingGroupParams](#cfn-iot-mitigationaction-actionparams-addthingstothinggroupparams)" : AddThingsToThingGroupParams,
  "[EnableIoTLoggingParams](#cfn-iot-mitigationaction-actionparams-enableiotloggingparams)" : EnableIoTLoggingParams,
  "[PublishFindingToSnsParams](#cfn-iot-mitigationaction-actionparams-publishfindingtosnsparams)" : PublishFindingToSnsParams,
  "[ReplaceDefaultPolicyVersionParams](#cfn-iot-mitigationaction-actionparams-replacedefaultpolicyversionparams)" : ReplaceDefaultPolicyVersionParams,
  "[UpdateCACertificateParams](#cfn-iot-mitigationaction-actionparams-updatecacertificateparams)" : UpdateCACertificateParams,
  "[UpdateDeviceCertificateParams](#cfn-iot-mitigationaction-actionparams-updatedevicecertificateparams)" : UpdateDeviceCertificateParams
}
```

### YAML<a name="aws-properties-iot-mitigationaction-actionparams-syntax.yaml"></a>

```
  [AddThingsToThingGroupParams](#cfn-iot-mitigationaction-actionparams-addthingstothinggroupparams): 
    AddThingsToThingGroupParams
  [EnableIoTLoggingParams](#cfn-iot-mitigationaction-actionparams-enableiotloggingparams): 
    EnableIoTLoggingParams
  [PublishFindingToSnsParams](#cfn-iot-mitigationaction-actionparams-publishfindingtosnsparams): 
    PublishFindingToSnsParams
  [ReplaceDefaultPolicyVersionParams](#cfn-iot-mitigationaction-actionparams-replacedefaultpolicyversionparams): 
    ReplaceDefaultPolicyVersionParams
  [UpdateCACertificateParams](#cfn-iot-mitigationaction-actionparams-updatecacertificateparams): 
    UpdateCACertificateParams
  [UpdateDeviceCertificateParams](#cfn-iot-mitigationaction-actionparams-updatedevicecertificateparams): 
    UpdateDeviceCertificateParams
```

## Properties<a name="aws-properties-iot-mitigationaction-actionparams-properties"></a>

`AddThingsToThingGroupParams`  <a name="cfn-iot-mitigationaction-actionparams-addthingstothinggroupparams"></a>
Specifies the group to which you want to add the devices\.  
*Required*: No  
*Type*: [AddThingsToThingGroupParams](aws-properties-iot-mitigationaction-addthingstothinggroupparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableIoTLoggingParams`  <a name="cfn-iot-mitigationaction-actionparams-enableiotloggingparams"></a>
Specifies the logging level and the role with permissions for logging\. You cannot specify a logging level of `DISABLED`\.  
*Required*: No  
*Type*: [EnableIoTLoggingParams](aws-properties-iot-mitigationaction-enableiotloggingparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublishFindingToSnsParams`  <a name="cfn-iot-mitigationaction-actionparams-publishfindingtosnsparams"></a>
Specifies the topic to which the finding should be published\.  
*Required*: No  
*Type*: [PublishFindingToSnsParams](aws-properties-iot-mitigationaction-publishfindingtosnsparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceDefaultPolicyVersionParams`  <a name="cfn-iot-mitigationaction-actionparams-replacedefaultpolicyversionparams"></a>
Replaces the policy version with a default or blank policy\. You specify the template name\. Only a value of `BLANK_POLICY` is currently supported\.  
*Required*: No  
*Type*: [ReplaceDefaultPolicyVersionParams](aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateCACertificateParams`  <a name="cfn-iot-mitigationaction-actionparams-updatecacertificateparams"></a>
Specifies the new state for the CA certificate\. Only a value of `DEACTIVATE` is currently supported\.  
*Required*: No  
*Type*: [UpdateCACertificateParams](aws-properties-iot-mitigationaction-updatecacertificateparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateDeviceCertificateParams`  <a name="cfn-iot-mitigationaction-actionparams-updatedevicecertificateparams"></a>
Specifies the new state for a device certificate\. Only a value of `DEACTIVATE` is currently supported\.  
*Required*: No  
*Type*: [UpdateDeviceCertificateParams](aws-properties-iot-mitigationaction-updatedevicecertificateparams.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)