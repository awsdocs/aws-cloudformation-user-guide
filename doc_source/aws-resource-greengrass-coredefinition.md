# AWS::Greengrass::CoreDefinition<a name="aws-resource-greengrass-coredefinition"></a>

The `AWS::Greengrass::CoreDefinition` resource represents a core definition for AWS IoT Greengrass\. Core definitions are used to organize your core definition versions\.

Core definitions can reference multiple core definition versions\. All core definition versions must be associated with a core definition\. Each core definition version can contain one Greengrass core\.

**Note**  
When you create a core definition, you can optionally include an initial core definition version\. To associate a core definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html) resource and specify the ID of this core definition\.  
After you create the core definition version that contains the core you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-coredefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-coredefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::CoreDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-coredefinition-initialversion)" : CoreDefinitionVersion,
      "[Name](#cfn-greengrass-coredefinition-name)" : String,
      "[Tags](#cfn-greengrass-coredefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-coredefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::CoreDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-coredefinition-initialversion): 
    CoreDefinitionVersion
  [Name](#cfn-greengrass-coredefinition-name): String
  [Tags](#cfn-greengrass-coredefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-coredefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-coredefinition-initialversion"></a>
The core definition version to include when the core definition is created\. Currently, a core definition version can contain only one [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-coredefinition-core.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-coredefinition-core.html)\.  
To associate a core definition version after the core definition is created, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html) resource and specify the ID of this core definition\.
*Required*: No  
*Type*: [CoreDefinitionVersion](aws-properties-greengrass-coredefinition-coredefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-coredefinition-name"></a>
The name of the core definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-coredefinition-tags"></a>
Application\-specific metadata to attach to the core definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
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

## Return values<a name="aws-resource-greengrass-coredefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-coredefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the core definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-coredefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-coredefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `CoreDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `CoreDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `CoreDefinitionVersion` that was added to the `CoreDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `CoreDefinition`, such as `MyCoreDefinition`\. 

## Examples<a name="aws-resource-greengrass-coredefinition--examples"></a>



### Create a Core Definition<a name="aws-resource-greengrass-coredefinition--examples--Create_a_Core_Definition"></a>

The following example creates a core definition that specifies an initial version that contains a core\.

The template uses the `Ref` function to return the ID of the core definition for the `CoreDefinitionId` property, which associates the version with the core definition\. The template uses parameters to represent the core definition name and the ID, thing ARN, and certificate ARN to use for the core\. It also outputs the ID of the new core definition\.

For another template example, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-coredefinition--examples--Create_a_Core_Definition--json"></a>

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

#### YAML<a name="aws-resource-greengrass-coredefinition--examples--Create_a_Core_Definition--yaml"></a>

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

## See also<a name="aws-resource-greengrass-coredefinition--seealso"></a>
+  [CreateCoreDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createcoredefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 