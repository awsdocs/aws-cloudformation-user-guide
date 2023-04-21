# AWS::IoTCoreDeviceAdvisor::SuiteDefinition SuiteDefinitionConfiguration<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration"></a>

<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-description"></a>The `SuiteDefinitionConfiguration` property type specifies Property description not available\. for an [AWS::IoTCoreDeviceAdvisor::SuiteDefinition](aws-resource-iotcoredeviceadvisor-suitedefinition.md)\.

## Syntax<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-syntax.json"></a>

```
{
  "[DevicePermissionRoleArn](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devicepermissionrolearn)" : String,
  "[Devices](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devices)" : [ DeviceUnderTest, ... ],
  "[IntendedForQualification](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-intendedforqualification)" : Boolean,
  "[RootGroup](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-rootgroup)" : String,
  "[SuiteDefinitionName](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-suitedefinitionname)" : String
}
```

### YAML<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-syntax.yaml"></a>

```
  [DevicePermissionRoleArn](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devicepermissionrolearn): String
  [Devices](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devices): 
    - DeviceUnderTest
  [IntendedForQualification](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-intendedforqualification): Boolean
  [RootGroup](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-rootgroup): String
  [SuiteDefinitionName](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-suitedefinitionname): String
```

## Properties<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-properties"></a>

`DevicePermissionRoleArn`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devicepermissionrolearn"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Devices`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-devices"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [DeviceUnderTest](aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntendedForQualification`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-intendedforqualification"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RootGroup`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-rootgroup"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuiteDefinitionName`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration-suitedefinitionname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)