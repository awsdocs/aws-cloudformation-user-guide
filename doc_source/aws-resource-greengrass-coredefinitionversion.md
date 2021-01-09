# AWS::Greengrass::CoreDefinitionVersion<a name="aws-resource-greengrass-coredefinitionversion"></a>

The `AWS::Greengrass::CoreDefinitionVersion` resource represents a core definition version for AWS IoT Greengrass\. A core definition version contains a Greengrass core\.

**Note**  
To create a core definition version, you must specify the ID of the core definition that you want to associate with the version\. For information about creating a core definition, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)\.  
After you create a core definition version that contains the core you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-coredefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-coredefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::CoreDefinitionVersion",
  "Properties" : {
      "[CoreDefinitionId](#cfn-greengrass-coredefinitionversion-coredefinitionid)" : String,
      "[Cores](#cfn-greengrass-coredefinitionversion-cores)" : [ Core, ... ]
    }
}
```

### YAML<a name="aws-resource-greengrass-coredefinitionversion-syntax.yaml"></a>

```
Type: AWS::Greengrass::CoreDefinitionVersion
Properties: 
  [CoreDefinitionId](#cfn-greengrass-coredefinitionversion-coredefinitionid): String
  [Cores](#cfn-greengrass-coredefinitionversion-cores): 
    - Core
```

## Properties<a name="aws-resource-greengrass-coredefinitionversion-properties"></a>

`CoreDefinitionId`  <a name="cfn-greengrass-coredefinitionversion-coredefinitionid"></a>
The ID of the core definition associated with this version\. This value is a GUID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Cores`  <a name="cfn-greengrass-coredefinitionversion-cores"></a>
The Greengrass core in this version\. Currently, the `Cores` property for a core definition version can contain only one core\.  
*Required*: Yes  
*Type*: List of [Core](aws-properties-greengrass-coredefinitionversion-core.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrass-coredefinitionversion-return-values"></a>

### Ref<a name="aws-resource-greengrass-coredefinitionversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the core definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-greengrass-coredefinitionversion--examples"></a>



### Create a Core Definition Version<a name="aws-resource-greengrass-coredefinitionversion--examples--Create_a_Core_Definition_Version"></a>

The following example creates two resources: a core definition and a core definition version that contains a core\.

The template uses the `Ref` function to provide the `CoreDefinitionId` for the core definition version \(which associates the version with the core definition\)\. The template uses parameters to represent the core definition name and the ID, thing ARN, and certificate ARN to use for the core\. It also outputs the ID of the new core definition and the ARN of the new core definition version\.

For another template example, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-coredefinitionversion--examples--Create_a_Core_Definition_Version--json"></a>

```
{
    "Description": "Create CoreDefinition and associated CoreDefinitionVersion",
    "Parameters": {
        "CoreDefinitionName": {
            "Type": "String",
            "Default": "TestCoreDefinition"
        },
        "CoreId": {
            "Type": "String",
            "Default": "TestCoreId"
        },
        "CoreThingArn": {
            "Type": "String",
            "Default": "TestCoreThingArn"
        },
        "CoreCertificateArn": {
            "Type": "String",
            "Default": "TestCoreCertArn"
        }
    },
    "Resources": {
        "CoreDefinition": {
            "Type": "AWS::Greengrass::CoreDefinition",
            "Properties": {
                "Name": {
                    "Ref": "CoreDefinitionName"
                }
            }
        },
        "CoreDefinitionVersion": {
            "Type": "AWS::Greengrass::CoreDefinitionVersion",
            "Properties": {
                "CoreDefinitionId": {
                    "Ref": "CoreDefinition"
                },
                "Cores": [
                    {
                        "Id": {
                            "Ref": "CoreId"
                        },
                        "CertificateArn": {
                            "Ref": "CoreCertificateArn"
                        },
                        "ThingArn": {
                            "Ref": "CoreThingArn"
                        },
                        "SyncShadow": "true"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "CoreDefinitionId": {
            "Value": {
                "Ref": "CoreDefinition"
            }
        },
        "CoreDefinitionVersionArn": {
            "Value": {
                "Ref": "CoreDefinitionVersion"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-coredefinitionversion--examples--Create_a_Core_Definition_Version--yaml"></a>

```
Description: Create CoreDefinition and associated CoreDefinitionVersion
Parameters:
  CoreDefinitionName:
    Type: String
    Default: TestCoreDefinition
  CoreId:
    Type: String
    Default: TestCoreId
  CoreThingArn:
    Type: String
    Default: TestCoreThingArn
  CoreCertificateArn:
    Type: String
    Default: TestCoreCertArn
Resources:
  CoreDefinition:
    Type: 'AWS::Greengrass::CoreDefinition'
    Properties:
      Name: !Ref CoreDefinitionName
  CoreDefinitionVersion:
    Type: 'AWS::Greengrass::CoreDefinitionVersion'
    Properties:
      CoreDefinitionId: !Ref CoreDefinition
      Cores:
        - Id: !Ref CoreId
          CertificateArn: !Ref CoreCertificateArn
          ThingArn: !Ref CoreThingArn
          SyncShadow: 'true'
Outputs:
  CoreDefinitionId:
    Value: !Ref CoreDefinition
  CoreDefinitionVersionArn:
    Value: !Ref CoreDefinitionVersion
```

## See also<a name="aws-resource-greengrass-coredefinitionversion--seealso"></a>
+  [CreateCoreDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/createcoredefinitionversion-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 