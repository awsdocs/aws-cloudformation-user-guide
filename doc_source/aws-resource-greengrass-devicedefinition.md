# AWS::Greengrass::DeviceDefinition<a name="aws-resource-greengrass-devicedefinition"></a>

The `AWS::Greengrass::DeviceDefinition` resource represents a device definition for AWS IoT Greengrass\. Device definitions are used to organize your device definition versions\.

Device definitions can reference multiple device definition versions\. All device definition versions must be associated with a device definition\. Each device definition version can contain one or more devices\.

**Note**  
When you create a device definition, you can optionally include an initial device definition version\. To associate a device definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html) resource and specify the ID of this device definition\.  
After you create the device definition version that contains the devices you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-devicedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-devicedefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::DeviceDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-devicedefinition-initialversion)" : DeviceDefinitionVersion,
      "[Name](#cfn-greengrass-devicedefinition-name)" : String,
      "[Tags](#cfn-greengrass-devicedefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-devicedefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::DeviceDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-devicedefinition-initialversion): 
    DeviceDefinitionVersion
  [Name](#cfn-greengrass-devicedefinition-name): String
  [Tags](#cfn-greengrass-devicedefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-devicedefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-devicedefinition-initialversion"></a>
The device definition version to include when the device definition is created\. A device definition version contains a list of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-devicedefinition-device.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-devicedefinition-device.html) property types\.  
To associate a device definition version after the device definition is created, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html) resource and specify the ID of this device definition\.
*Required*: No  
*Type*: [DeviceDefinitionVersion](aws-properties-greengrass-devicedefinition-devicedefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-devicedefinition-name"></a>
The name of the device definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-devicedefinition-tags"></a>
Application\-specific metadata to attach to the device definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
This `Json` property type is processed as a map of key\-value pairs\. It uses the following format, which is different from most `Tags` implementations in AWS CloudFormation templates\.  

```
"Tags": {
    "KeyName0": "value",
    "KeyName1": "value",
    "KeyName2": "value"
}
```
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-greengrass-devicedefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-devicedefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the device definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-devicedefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-devicedefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `DeviceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `DeviceDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `DeviceDefinitionVersion` that was added to the `DeviceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the device definition\.

## Examples<a name="aws-resource-greengrass-devicedefinition--examples"></a>



### Device Definition Snippet<a name="aws-resource-greengrass-devicedefinition--examples--Device_Definition_Snippet"></a>

The following snippet defines a device definition resource with an initial version that contains a device\. This example points to a manually generated device certificate\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-devicedefinition--examples--Device_Definition_Snippet--json"></a>

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

#### YAML<a name="aws-resource-greengrass-devicedefinition--examples--Device_Definition_Snippet--yaml"></a>

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

## See also<a name="aws-resource-greengrass-devicedefinition--seealso"></a>
+  [CreateDeviceDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createdevicedefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 