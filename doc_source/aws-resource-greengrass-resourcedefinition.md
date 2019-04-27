# AWS::Greengrass::ResourceDefinition<a name="aws-resource-greengrass-resourcedefinition"></a>

The `AWS::Greengrass::ResourceDefinition` resource represents a resource definition for AWS IoT Greengrass\. Resource definitions are used to organize your resource definition versions\.

Resource definitions can reference multiple resource definition versions\.

![\[A resource definition hierarchy with associated resource definition versions and resources.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-resource.png)

All resource definition versions must be associated with a resource definition\. Each resource definition version can contain one or more resources\. \(In AWS CloudFormation, resources are named *resource instances*\.\)

**Note**  
When you create a resource definition, you can optionally include an initial resource definition version\. To associate a resource definition version later, create an [AWS::Greengrass::ResourceDefinitionVersion](aws-resource-greengrass-resourcedefinitionversion.md) resource and specify the ID of this resource definition\.  
After you create the resource definition version that contains the resources you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-resourcedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-resourcedefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ResourceDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-resourcedefinition-initialversion)" : [*ResourceDefinitionVersion*](aws-properties-greengrass-resourcedefinition-resourcedefinitionversion.md),
    "[Name](#cfn-greengrass-resourcedefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-resourcedefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::ResourceDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-resourcedefinition-initialversion): 
    [*ResourceDefinitionVersion*](aws-properties-greengrass-resourcedefinition-resourcedefinitionversion.md)
  [Name](#cfn-greengrass-resourcedefinition-name): String
```

## Properties<a name="aws-resource-greengrass-resourcedefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-resourcedefinition-initialversion"></a>
The resource definition version to include when the resource definition is created\. A resource definition version contains a list of [`resource instance`](aws-properties-greengrass-resourcedefinition-resourceinstance.md) property types\.  
To associate a resource definition version after the resource definition is created, create an [AWS::Greengrass::ResourceDefinitionVersion](aws-resource-greengrass-resourcedefinitionversion.md) resource and specify the ID of this resource definition\.
 *Required*: No  
 *Type*: [ResourceDefinitionVersion](aws-properties-greengrass-resourcedefinition-resourcedefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-resourcedefinition-name"></a>
The name of the resource definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-resourcedefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-resourcedefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::ResourceDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the resource definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-resourcedefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `ResourceDefinitionVersion` that was added to the `ResourceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `ResourceDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `ResourceDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `ResourceDefinition`, such as `MyResourceDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-resourcedefinition-examples"></a>

### Resource Definition Snippet<a name="aws-resource-greengrass-resourcedefinition-example1"></a>

The following snippet defines a resource definition resource with an initial version that contains each type of resource\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-resourcedefinition-example1.json"></a>

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

#### YAML<a name="aws-resource-greengrass-resourcedefinition-example1.yaml"></a>

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

## See Also<a name="aws-resource-greengrass-resourcedefinition-seealso"></a>
+ [CreateResourceDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createresourcedefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)