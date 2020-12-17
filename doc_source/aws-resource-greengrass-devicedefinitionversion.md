# AWS::Greengrass::DeviceDefinitionVersion<a name="aws-resource-greengrass-devicedefinitionversion"></a>

The `AWS::Greengrass::DeviceDefinitionVersion` resource represents a device definition version for AWS IoT Greengrass\. A device definition version contains a list of devices\.

**Note**  
To create a device definition version, you must specify the ID of the device definition that you want to associate with the version\. For information about creating a device definition, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)\.  
After you create a device definition version that contains the devices you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-devicedefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-devicedefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::DeviceDefinitionVersion",
  "Properties" : {
      "[DeviceDefinitionId](#cfn-greengrass-devicedefinitionversion-devicedefinitionid)" : String,
      "[Devices](#cfn-greengrass-devicedefinitionversion-devices)" : [ Device, ... ]
    }
}
```

### YAML<a name="aws-resource-greengrass-devicedefinitionversion-syntax.yaml"></a>

```
Type: AWS::Greengrass::DeviceDefinitionVersion
Properties: 
  [DeviceDefinitionId](#cfn-greengrass-devicedefinitionversion-devicedefinitionid): String
  [Devices](#cfn-greengrass-devicedefinitionversion-devices): 
    - Device
```

## Properties<a name="aws-resource-greengrass-devicedefinitionversion-properties"></a>

`DeviceDefinitionId`  <a name="cfn-greengrass-devicedefinitionversion-devicedefinitionid"></a>
The ID of the device definition associated with this version\. This value is a GUID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Devices`  <a name="cfn-greengrass-devicedefinitionversion-devices"></a>
The devices in this version\.  
*Required*: Yes  
*Type*: List of [Device](aws-properties-greengrass-devicedefinitionversion-device.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrass-devicedefinitionversion-return-values"></a>

### Ref<a name="aws-resource-greengrass-devicedefinitionversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the device definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-greengrass-devicedefinitionversion--examples"></a>



### Device Definition Version Snippet<a name="aws-resource-greengrass-devicedefinitionversion--examples--Device_Definition_Version_Snippet"></a>

The following snippet defines device definition and device definition version resources\. The device definition version references the device definition and contains a device\. This example points to a manually generated device certificate\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-devicedefinitionversion--examples--Device_Definition_Version_Snippet--json"></a>

```
"TestDeviceDefinition": {
    "Type": "AWS::Greengrass::DeviceDefinition",
    "Properties": {
        "Name": "DemoTestDeviceDefinition"
    }
},
"TestDeviceDefinitionVersion": {
    "Type": "AWS::Greengrass::DeviceDefinitionVersion",
    "Properties": {
        "DeviceDefinitionId": {
            "Fn::GetAtt": [
                "TestDeviceDefinition",
                "Id"
            ]
        },
        "Devices": [
            {
                "Id": "TestDevice1",
                "CertificateArn": {
                    "Fn::Join": [
                        ":",
                        [
                            "arn:aws:iot",
                            {
                                "Ref": "AWS::Region"
                            },
                            {
                                "Ref": "AWS::AccountId"
                            },
                            "cert/4db8b7f58d95b7fdb45c38c28a0b1adf6c5f8c03e902de65734935fea83e751f"
                        ]
                    ]
                },
                "SyncShadow": "true",
                "ThingArn": {
                    "Fn::Join": [
                        ":",
                        [
                            "arn:aws:iot",
                            {
                                "Ref": "AWS::Region"
                            },
                            {
                                "Ref": "AWS::AccountId"
                            },
                            "thing/TestDevice1"
                        ]
                    ]
                }
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-greengrass-devicedefinitionversion--examples--Device_Definition_Version_Snippet--yaml"></a>

```
TestDeviceDefinition:
  Type: 'AWS::Greengrass::DeviceDefinition'
  Properties:
    Name: DemoTestDeviceDefinition
TestDeviceDefinitionVersion:
  Type: 'AWS::Greengrass::DeviceDefinitionVersion'
  Properties:
    DeviceDefinitionId: !GetAtt 
      - TestDeviceDefinition
      - Id
    Devices:
      - Id: TestDevice1
        CertificateArn: !Join 
          - ':'
          - - 'arn:aws:iot'
            - !Ref 'AWS::Region'
            - !Ref 'AWS::AccountId'
            - >-
              cert/4db8b7f58d95b7fdb45c38c28a0b1adf6c5f8c03e902de65734935fea83e751f
        SyncShadow: 'true'
        ThingArn: !Join 
          - ':'
          - - 'arn:aws:iot'
            - !Ref 'AWS::Region'
            - !Ref 'AWS::AccountId'
            - thing/TestDevice1
```

## See also<a name="aws-resource-greengrass-devicedefinitionversion--seealso"></a>
+  [CreateDeviceDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/createdevicedefinitionversion-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 