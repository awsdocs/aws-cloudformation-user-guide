# AWS::Greengrass::DeviceDefinition<a name="aws-resource-greengrass-devicedefinition"></a>

The `AWS::Greengrass::DeviceDefinition` resource represents a device definition for AWS IoT Greengrass\. Device definitions are used to organize your device definition versions\.

Device definitions can reference multiple device definition versions\.

![\[A device definition hierarchy with associated device definition versions and devices.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-device.png)

All device definition versions must be associated with a device definition\. Each device definition version can contain one or more devices\.

**Note**  
When you create a device definition, you can optionally include an initial device definition version\. To associate a device definition version later, create an [AWS::Greengrass::DeviceDefinitionVersion](aws-resource-greengrass-devicedefinitionversion.md) resource and specify the ID of this device definition\.  
After you create the device definition version that contains the devices you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-devicedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-devicedefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::DeviceDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-devicedefinition-initialversion)" : [*DeviceDefinitionVersion*](aws-properties-greengrass-devicedefinition-devicedefinitionversion.md),
    "[Name](#cfn-greengrass-devicedefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-devicedefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::DeviceDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-devicedefinition-initialversion):
    [*DeviceDefinitionVersion*](aws-properties-greengrass-devicedefinition-devicedefinitionversion.md)
  [Name](#cfn-greengrass-devicedefinition-name): String
```

## Properties<a name="aws-resource-greengrass-devicedefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-devicedefinition-initialversion"></a>
The device definition version to include when the device definition is created\. A device definition version contains a list of [`device`](aws-properties-greengrass-devicedefinition-device.md) property types\.  
To associate a device definition version after the device definition is created, create an [AWS::Greengrass::DeviceDefinitionVersion](aws-resource-greengrass-devicedefinitionversion.md) resource and specify the ID of this device definition\.
 *Required*: No  
 *Type*: [DeviceDefinitionVersion](aws-properties-greengrass-devicedefinition-devicedefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-devicedefinition-name"></a>
The name of the device definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-devicedefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-devicedefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::DeviceDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the device definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-devicedefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `DeviceDefinitionVersion` that was added to the `DeviceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `DeviceDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `DeviceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `DeviceDefinition`, such as `MyDeviceDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-devicedefinition-examples"></a>

### Device Definition Snippet<a name="aws-resource-greengrass-devicedefinition-example1"></a>

The following snippet defines a device definition resource with an initial version that contains a device\. This example points to a manually generated device certificate\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-devicedefinition-example1.json"></a>

```
"TestDeviceDefinition": {
    "Type": "AWS::Greengrass::DeviceDefinition",
    "Properties": {
        "Name": "DemoTestDeviceDefinition",
        "InitialVersion": {
            "Devices": [
                {
                    "Id": "TestDevice1",
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
                    },
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
                    "SyncShadow": "true"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-devicedefinition-example1.yaml"></a>

```
TestDeviceDefinition:
  Type: 'AWS::Greengrass::DeviceDefinition'
  Properties:
    Name: DemoTestDeviceDefinition
    InitialVersion:
      Devices:
        - Id: TestDevice1
          ThingArn: !Join 
            - ':'
            - - 'arn:aws:iot'
              - !Ref 'AWS::Region'
              - !Ref 'AWS::AccountId'
              - thing/TestDevice1
          CertificateArn: !Join 
            - ':'
            - - 'arn:aws:iot'
              - !Ref 'AWS::Region'
              - !Ref 'AWS::AccountId'
              - >-
                cert/4db8b7f58d95b7fdb45c38c28a0b1adf6c5f8c03e902de65734935fea83e751f
          SyncShadow: 'true'
```

## See Also<a name="aws-resource-greengrass-devicedefinition-seealso"></a>
+ [CreateDeviceDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createdevicedefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)