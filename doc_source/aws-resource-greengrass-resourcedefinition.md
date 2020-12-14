# AWS::Greengrass::ResourceDefinition<a name="aws-resource-greengrass-resourcedefinition"></a>

The `AWS::Greengrass::ResourceDefinition` resource represents a resource definition for AWS IoT Greengrass\. Resource definitions are used to organize your resource definition versions\.

Resource definitions can reference multiple resource definition versions\. All resource definition versions must be associated with a resource definition\. Each resource definition version can contain one or more resources\. \(In AWS CloudFormation, resources are named *resource instances*\.\)

**Note**  
When you create a resource definition, you can optionally include an initial resource definition version\. To associate a resource definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html) resource and specify the ID of this resource definition\.  
After you create the resource definition version that contains the resources you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-resourcedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-resourcedefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ResourceDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-resourcedefinition-initialversion)" : ResourceDefinitionVersion,
      "[Name](#cfn-greengrass-resourcedefinition-name)" : String,
      "[Tags](#cfn-greengrass-resourcedefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-resourcedefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::ResourceDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-resourcedefinition-initialversion): 
    ResourceDefinitionVersion
  [Name](#cfn-greengrass-resourcedefinition-name): String
  [Tags](#cfn-greengrass-resourcedefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-resourcedefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-resourcedefinition-initialversion"></a>
The resource definition version to include when the resource definition is created\. A resource definition version contains a list of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourceinstance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourceinstance.html) property types\.  
To associate a resource definition version after the resource definition is created, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html) resource and specify the ID of this resource definition\.
*Required*: No  
*Type*: [ResourceDefinitionVersion](aws-properties-greengrass-resourcedefinition-resourcedefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-resourcedefinition-name"></a>
The name of the resource definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-resourcedefinition-tags"></a>
Application\-specific metadata to attach to the resource definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
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

## Return values<a name="aws-resource-greengrass-resourcedefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-resourcedefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the resource definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-resourcedefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-resourcedefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `ResourceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `ResourceDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\.

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `ResourceDefinitionVersion` that was added to the `ResourceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `ResourceDefinition`, such as `MyResourceDefinition`\.

## Examples<a name="aws-resource-greengrass-resourcedefinition--examples"></a>



### Resource Definition Snippet<a name="aws-resource-greengrass-resourcedefinition--examples--Resource_Definition_Snippet"></a>

The following snippet defines a resource definition resource with an initial version that contains each type of resource\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-resourcedefinition--examples--Resource_Definition_Snippet--json"></a>

```
"TestResourceDefinition": {
    "Type": "AWS::Greengrass::ResourceDefinition",
    "Properties": {
        "Name": "DemoTestResourceDefinition",
        "InitialVersion": {
            "Resources": [
                {
                    "Id": "ResourceId1",
                    "Name": "LocalDeviceResource",
                    "ResourceDataContainer": {
                        "LocalDeviceResourceData": {
                            "SourcePath": "/dev/TestSourcePath1",
                            "GroupOwnerSetting": {
                                "AutoAddGroupOwner": "false",
                                "GroupOwner": "TestOwner"
                            }
                        }
                    }
                },
                {
                    "Id": "ResourceId2",
                    "Name": "LocalVolumeResourceData",
                    "ResourceDataContainer": {
                        "LocalVolumeResourceData": {
                            "SourcePath": "/dev/TestSourcePath2",
                            "DestinationPath": "/volumes/TestDestinationPath2",
                            "GroupOwnerSetting": {
                                "AutoAddGroupOwner": "false",
                                "GroupOwner": "TestOwner"
                            }
                        }
                    }
                },
                {
                    "Id": "ResourceId3",
                    "Name": "SageMakerMachineLearningModelResourceData",
                    "ResourceDataContainer": {
                        "SageMakerMachineLearningModelResourceData": {
                            "SageMakerJobArn": {
                                "Fn::Join": [
                                    ":",
                                    [
                                        "arn:aws:sagemaker",
                                        {
                                            "Ref": "AWS::Region"
                                        },
                                        {
                                            "Ref": "AWS::AccountId"
                                        },
                                        "training-job/testJob"
                                    ]
                                ]
                            },
                            "DestinationPath": "/sagemakermodels/TestDestinationPath3"
                        }
                    }
                },
                {
                    "Id": "ResourceId4",
                    "Name": "S3MachineLearningModelResourceData",
                    "ResourceDataContainer": {
                        "S3MachineLearningModelResourceData": {
                            "S3Uri": "http://testBucket.s3.amazonaws.com/testUri.zip",
                            "DestinationPath": "/mlModels/TestDestinationPath4"
                        }
                    }
                },
                {
                    "Id": "ResourceId5",
                    "Name": "SecretsManagerSecretResourceData",
                    "ResourceDataContainer": {
                        "SecretsManagerSecretResourceData": {
                            "ARN": {
                                "Fn::Join": [
                                    ":",
                                    [
                                        "arn:aws:secretsmanager",
                                        {
                                            "Ref": "AWS::Region"
                                        },
                                        {
                                            "Ref": "AWS::AccountId"
                                        },
                                        "secret:testARN"
                                    ]
                                ]
                            },
                            "AdditionalStagingLabelsToDownload": [
                                "label1",
                                "label2"
                            ]
                        }
                    }
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-resourcedefinition--examples--Resource_Definition_Snippet--yaml"></a>

```
TestResourceDefinition:
  Type: 'AWS::Greengrass::ResourceDefinition'
  Properties:
    Name: DemoTestResourceDefinition
TestResourceDefinitionVersion:
  Type: 'AWS::Greengrass::ResourceDefinitionVersion'
  Properties:
    ResourceDefinitionId: !Ref TestResourceDefinition
    Resources:
      - Id: ResourceId1
        Name: LocalDeviceResource
        ResourceDataContainer:
          LocalDeviceResourceData:
            SourcePath: /dev/TestSourcePath1
            GroupOwnerSetting:
              AutoAddGroupOwner: 'false'
              GroupOwner: TestOwner
      - Id: ResourceId2
        Name: LocalVolumeResourceData
        ResourceDataContainer:
          LocalVolumeResourceData:
            SourcePath: /dev/TestSourcePath2
            DestinationPath: /volumes/TestDestinationPath2
            GroupOwnerSetting:
              AutoAddGroupOwner: 'false'
              GroupOwner: TestOwner
      - Id: ResourceId3
        Name: SageMakerMachineLearningModelResourceData
        ResourceDataContainer:
          SageMakerMachineLearningModelResourceData:
            SageMakerJobArn: !Join 
              - ':'
              - - 'arn:aws:sagemaker'
                - !Ref 'AWS::Region'
                - !Ref 'AWS::AccountId'
                - training-job/testJob
            DestinationPath: /sagemakermodels/TestDestinationPath3
      - Id: ResourceId4
        Name: S3MachineLearningModelResourceData
        ResourceDataContainer:
          S3MachineLearningModelResourceData:
            S3Uri: 'http://testBucket.s3.amazonaws.com/testUri.zip'
            DestinationPath: /mlModels/TestDestinationPath4
      - Id: ResourceId5
        Name: SecretsManagerSecretResourceData
        ResourceDataContainer:
          SecretsManagerSecretResourceData:
            ARN: !Join 
              - ':'
              - - 'arn:aws:secretsmanager'
                - !Ref 'AWS::Region'
                - !Ref 'AWS::AccountId'
                - 'secret:testARN'
            AdditionalStagingLabelsToDownload:
              - label1
              - label2
```

## See also<a name="aws-resource-greengrass-resourcedefinition--seealso"></a>
+  [CreateResourceDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createresourcedefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 