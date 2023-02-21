# AWS::IoTCoreDeviceAdvisor::SuiteDefinition<a name="aws-resource-iotcoredeviceadvisor-suitedefinition"></a>

Creates a Device Advisor test suite\.

Requires permission to access the [CreateSuiteDefinition](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions) action\.

## Syntax<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-syntax.json"></a>

```
{
  "Type" : "AWS::IoTCoreDeviceAdvisor::SuiteDefinition",
  "Properties" : {
      "[SuiteDefinitionConfiguration](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration)" : SuiteDefinitionConfiguration,
      "[Tags](#cfn-iotcoredeviceadvisor-suitedefinition-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-syntax.yaml"></a>

```
Type: AWS::IoTCoreDeviceAdvisor::SuiteDefinition
Properties: 
  [SuiteDefinitionConfiguration](#cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration): 
    SuiteDefinitionConfiguration
  [Tags](#cfn-iotcoredeviceadvisor-suitedefinition-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-properties"></a>

`SuiteDefinitionConfiguration`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration"></a>
The configuration of the Suite Definition\. Listed below are the required elements of the `SuiteDefinitionConfiguration`\.    
**devicePermissionRoleArn**  
The device permission arn\.  
This is a required element\.  
**Type:** String  
**devices**  
The list of configured devices under test\. For more information on devices under test, see [DeviceUnderTest](http://amazonaws.com/iot/latest/apireference/API_iotdeviceadvisor_DeviceUnderTest.html)  
Not a required element\.  
**Type:** List of devices under test  
**intendedForQualification**  
The tests intended for qualification in a suite\.  
Not a required element\.  
**Type:** Boolean  
**rootGroup**  
The test suite root group\. For more information on creating and using root groups see the [Device Advisor workflow](https://docs.aws.amazon.com/iot/latest/developerguide/device-advisor-workflow.html)\.  
This is a required element\.  
**Type:** String  
**suiteDefinitionName**  
The Suite Definition Configuration name\.  
This is a required element\.  
**Type:** String
*Required*: Yes  
*Type*: [SuiteDefinitionConfiguration](aws-properties-iotcoredeviceadvisor-suitedefinition-suitedefinitionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotcoredeviceadvisor-suitedefinition-tags"></a>
Metadata that can be used to manage the the Suite Definition\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-return-values"></a>

### Ref<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Suite Definition name\.

### Fn::GetAtt<a name="aws-resource-iotcoredeviceadvisor-suitedefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotcoredeviceadvisor-suitedefinition-return-values-fn--getatt-fn--getatt"></a>

`SuiteDefinitionArn`  <a name="SuiteDefinitionArn-fn::getatt"></a>
The Arn of the Suite Definition\.

`SuiteDefinitionId`  <a name="SuiteDefinitionId-fn::getatt"></a>
The version of the Suite Definition\.

`SuiteDefinitionVersion`  <a name="SuiteDefinitionVersion-fn::getatt"></a>
The ID of the Suite Definition\.

## Examples<a name="aws-resource-iotcoredeviceadvisor-suitedefinition--examples"></a>

### <a name="aws-resource-iotcoredeviceadvisor-suitedefinition--examples--"></a>

The following example is a template of a `SuiteDefintion`\.

#### JSON<a name="aws-resource-iotcoredeviceadvisor-suitedefinition--examples----json"></a>

```
{
   "Resources": {
      "TestSuiteDefinition": {
         "Type": "AWS::IoTCoreDeviceAdvisor::SuiteDefinition",
         "Properties": {
            "SuiteDefinitionConfiguration": {
               "SuiteDefinitionName": "SuiteDefinitionName",
               "DevicePermissionRoleArn": "arn:aws:iam::123456789012:role/RoleName",
               "Devices": [
                  {
                     "ThingArn": "arn:aws:iot:us-east-1:123456789012:thing/ThingName"
                  }
               ],
               "RootGroup": "{\n\"configuration\": {},\n\"tests\": [{\n\"name\": \"TestGroup\",\n\"configuration\": {\n\"EXECUTION_TIMEOUT\": \"30\"\n},\n\"tests\": [{\n\"name\": \"MQTTPublishTest\",\n\"configuration\": {\n\"TOPIC_FOR_PUBLISH_VALIDATION\": \"target\"\n},\n\"test\": {\n\"id\": \"MQTT_Publish\",\n\"version\": \"0.0.0\"\n}\n}]\n}]\n}",
               "IntendedForQualification": false
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iotcoredeviceadvisor-suitedefinition--examples----yaml"></a>

```
Resources:
  TestSuiteDefinition:
    Type: 'AWS::IoTCoreDeviceAdvisor::SuiteDefinition'
    Properties:
      SuiteDefinitionConfiguration:
        SuiteDefinitionName: "SuiteDefinitionName" 
        DevicePermissionRoleArn: "arn:aws:iam::123456789012:role/RoleName" 
        Devices: 
          - ThingArn: "arn:aws:iot:us-east-1:123456789012:thing/ThingName"
        RootGroup: '{
                "configuration": {},
                "tests": [{
                    "name": "TestGroup",
                    "configuration": {
                        "EXECUTION_TIMEOUT": "30"
                    },
                    "tests": [{
                        "name": "MQTTPublishTest",
                        "configuration": {
                            "TOPIC_FOR_PUBLISH_VALIDATION": "target"
                        },
                        "test": {
                            "id": "MQTT_Publish",
                            "version": "0.0.0"
                        }
                    }]
                }]
            }'
        IntendedForQualification: false
```