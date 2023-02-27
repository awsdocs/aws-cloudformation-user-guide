# AWS::IoTCoreDeviceAdvisor::SuiteDefinition DeviceUnderTest<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest"></a>

Information of a test device\. A thing ARN or a certificate ARN is required\.

## Syntax<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-certificatearn)" : String,
  "[ThingArn](#cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-thingarn)" : String
}
```

### YAML<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest-syntax.yaml"></a>

```
  [CertificateArn](#cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-certificatearn): String
  [ThingArn](#cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-thingarn): String
```

## Properties<a name="aws-properties-iotcoredeviceadvisor-suitedefinition-deviceundertest-properties"></a>

`CertificateArn`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-certificatearn"></a>
Lists devices certificate ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingArn`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-deviceundertest-thingarn"></a>
Lists devices thing ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)