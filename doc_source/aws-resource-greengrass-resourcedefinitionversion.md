# AWS::Greengrass::ResourceDefinitionVersion<a name="aws-resource-greengrass-resourcedefinitionversion"></a>

The `AWS::Greengrass::ResourceDefinitionVersion` resource represents a resource definition version for AWS IoT Greengrass\. A resource definition version contains a list of resources\. \(In AWS CloudFormation, resources are named *resource instances*\.\)

**Note**  
To create a resource definition version, you must specify the ID of the resource definition that you want to associate with the version\. For information about creating a resource definition, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)\.  
After you create a resource definition version that contains the resources you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-resourcedefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-resourcedefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ResourceDefinitionVersion",
  "Properties" : {
      "[ResourceDefinitionId](#cfn-greengrass-resourcedefinitionversion-resourcedefinitionid)" : String,
      "[Resources](#cfn-greengrass-resourcedefinitionversion-resources)" : [ ResourceInstance, ... ]
    }
}
```

### YAML<a name="aws-resource-greengrass-resourcedefinitionversion-syntax.yaml"></a>

```
Type: AWS::Greengrass::ResourceDefinitionVersion
Properties: 
  [ResourceDefinitionId](#cfn-greengrass-resourcedefinitionversion-resourcedefinitionid): String
  [Resources](#cfn-greengrass-resourcedefinitionversion-resources): 
    - ResourceInstance
```

## Properties<a name="aws-resource-greengrass-resourcedefinitionversion-properties"></a>

`ResourceDefinitionId`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedefinitionid"></a>
The ID of the resource definition associated with this version\. This value is a GUID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resources`  <a name="cfn-greengrass-resourcedefinitionversion-resources"></a>
The resources in this version\.  
*Required*: Yes  
*Type*: List of [ResourceInstance](aws-properties-greengrass-resourcedefinitionversion-resourceinstance.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrass-resourcedefinitionversion-return-values"></a>

### Ref<a name="aws-resource-greengrass-resourcedefinitionversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the resource definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-greengrass-resourcedefinitionversion--examples"></a>



### Resource Definition Version Snippet<a name="aws-resource-greengrass-resourcedefinitionversion--examples--Resource_Definition_Version_Snippet"></a>

The following snippet defines resource definition and resource definition version resources\. The resource definition version references the resource definition and contains each type of resource\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-resourcedefinitionversion--examples--Resource_Definition_Version_Snippet--json"></a>

```
"TestResourceDefinition": {
    "Type": "AWS::Greengrass::ResourceDefinition",
    "Properties": {
        "Name": "DemoTestResourceDefinition"
    }
},
"TestResourceDefinitionVersion": {
    "Type": "AWS::Greengrass::ResourceDefinitionVersion",
    "Properties": {
        "ResourceDefinitionId": {
            "Ref": "TestResourceDefinition"
        },
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
```

#### YAML<a name="aws-resource-greengrass-resourcedefinitionversion--examples--Resource_Definition_Version_Snippet--yaml"></a>

```
TestResourceDefinition:
  Type: 'AWS::Greengrass::ResourceDefinition'
  Properties:
    Name: DemoTestResourceDefinition
    InitialVersion:
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

## See also<a name="aws-resource-greengrass-resourcedefinitionversion--seealso"></a>
+  [CreateResourceDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/createresourcedefinitionversion-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 