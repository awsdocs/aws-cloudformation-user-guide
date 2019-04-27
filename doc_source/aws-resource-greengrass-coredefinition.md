# AWS::Greengrass::CoreDefinition<a name="aws-resource-greengrass-coredefinition"></a>

The `AWS::Greengrass::CoreDefinition` resource represents a core definition for AWS IoT Greengrass\. Core definitions are used to organize your core definition versions\.

Core definitions can reference multiple core definition versions\.

![\[A core definition hierarchy with associated core definition versions and cores.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-core.png)

All core definition versions must be associated with a core definition\. Each core definition version can contain one Greengrass core\.

**Note**  
When you create a core definition, you can optionally include an initial core definition version\. To associate a core definition version later, create an [AWS::Greengrass::CoreDefinitionVersion](aws-resource-greengrass-coredefinitionversion.md) resource and specify the ID of this core definition\.  
After you create the core definition version that contains the core you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-coredefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-coredefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::CoreDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-coredefinition-initialversion)" : [*CoreDefinitionVersion*](aws-properties-greengrass-coredefinition-coredefinitionversion.md),
    "[Name](#cfn-greengrass-coredefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-coredefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::CoreDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-coredefinition-initialversion): 
    [*CoreDefinitionVersion*](aws-properties-greengrass-coredefinition-coredefinitionversion.md)
  [Name](#cfn-greengrass-coredefinition-name): String
```

## Properties<a name="aws-resource-greengrass-coredefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-coredefinition-initialversion"></a>
The core definition version to include when the core definition is created\. Currently, a core definition version can contain only one [`core`](aws-properties-greengrass-coredefinition-core.md)\.  
To associate a core definition version after the core definition is created, create an [AWS::Greengrass::CoreDefinitionVersion](aws-resource-greengrass-coredefinitionversion.md) resource and specify the ID of this core definition\.
 *Required*: No  
 *Type*: [CoreDefinitionVersion](aws-properties-greengrass-coredefinition-coredefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-coredefinition-name"></a>
The name of the core definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-coredefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-coredefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::CoreDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the core definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-coredefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `CoreDefinitionVersion` that was added to the `CoreDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `CoreDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `CoreDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `CoreDefinition`, such as `MyCoreDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-coredefinition-examples"></a>

### Create a Core Definition<a name="aws-resource-greengrass-coredefinition-example1"></a>

The following example creates a core definition that specifies an initial version that contains a core\.

The template uses the `Ref` function to return the ID of the core definition for the `CoreDefinitionId` property, which associates the version with the core definition\. The template uses parameters to represent the core definition name and the ID, thing ARN, and certificate ARN to use for the core\. It also outputs the ID of the new core definition\.

#### JSON<a name="aws-resource-greengrass-coredefinition-example1.json"></a>

```
{
    "Description": "Create CoreDefinition with InitialVersion",
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
                },
                "InitialVersion": {
                    "Cores": [
                        {
                            "Id": {
                                "Ref": "CoreId"
                            },
                            "ThingArn": {
                                "Ref": "CoreThingArn"
                            },
                            "CertificateArn": {
                                "Ref": "CoreCertificateArn"
                            },
                            "SyncShadow": "true"
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "CoreDefinitionId": {
            "Value": {
                "Ref": "CoreDefinition"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-coredefinition-example1.yaml"></a>

```
Description: Create CoreDefinition with InitialVersion
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
      InitialVersion:
        Cores:
          - Id: !Ref CoreId
            ThingArn: !Ref CoreThingArn
            CertificateArn: !Ref CoreCertificateArn
            SyncShadow: 'true'
Outputs:
  CoreDefinitionId:
    Value: !Ref CoreDefinition
```

## See Also<a name="aws-resource-greengrass-coredefinition-seealso"></a>
+ [CreateCoreDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createcoredefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)