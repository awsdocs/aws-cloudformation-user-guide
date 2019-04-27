# AWS::Greengrass::FunctionDefinitionVersion<a name="aws-resource-greengrass-functiondefinitionversion"></a>

The `AWS::Greengrass::FunctionDefinitionVersion` resource represents a function definition version for AWS IoT Greengrass\. A function definition version contains contain a list of functions\.

**Note**  
To create a function definition version, you must specify the ID of the function definition that you want to associate with the version\. For information about creating a function definition, see [AWS::Greengrass::FunctionDefinition](aws-resource-greengrass-functiondefinition.md)\.  
After you create a function definition version that contains the functions you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-functiondefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-functiondefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::FunctionDefinitionVersion",
  "Properties" : {
    "[DefaultConfig](#cfn-greengrass-functiondefinitionversion-defaultconfig)" : [*DefaultConfig*](aws-properties-greengrass-functiondefinitionversion-defaultconfig.md),
    "[Functions](#cfn-greengrass-functiondefinitionversion-functions)" : [ [*Function*](aws-properties-greengrass-functiondefinitionversion-function.md), ... ],
    "[FunctionDefinitionId](#cfn-greengrass-functiondefinitionversion-functiondefinitionid)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-functiondefinitionversion-syntax.yaml"></a>

```
Type: "AWS::Greengrass::FunctionDefinitionVersion"
Properties:
  [DefaultConfig](#cfn-greengrass-functiondefinitionversion-defaultconfig): 
    [*DefaultConfig*](aws-properties-greengrass-functiondefinitionversion-defaultconfig.md)
  [Functions](#cfn-greengrass-functiondefinitionversion-functions): 
    - [*Function*](aws-properties-greengrass-functiondefinitionversion-function.md)
  [FunctionDefinitionId](#cfn-greengrass-functiondefinitionversion-functiondefinitionid): String
```

## Properties<a name="aws-resource-greengrass-functiondefinitionversion-properties"></a>

`DefaultConfig`  <a name="cfn-greengrass-functiondefinitionversion-defaultconfig"></a>
The default configuration that applies to all Lambda functions in the group\. Individual Lambda functions can override these settings\.  
 *Required*: No  
 *Type*: [DefaultConfig](aws-properties-greengrass-functiondefinitionversion-defaultconfig.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Functions`  <a name="cfn-greengrass-functiondefinitionversion-functions"></a>
The functions in this version\.  
 *Required*: Yes  
 *Type*: List of [Function](aws-properties-greengrass-functiondefinitionversion-function.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FunctionDefinitionId`  <a name="cfn-greengrass-functiondefinitionversion-functiondefinitionid"></a>
The ID of the function definition associated with this version\. This value is a GUID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-greengrass-functiondefinitionversion-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-functiondefinitionversion-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::FunctionDefinitionVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the function definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-greengrass-functiondefinitionversion-examples"></a>

### Function Definition Version Snippet<a name="aws-resource-greengrass-functiondefinitionversion-example1"></a>

The following snippet defines function definition and function definition version resources\. The function definition version references the function definition and contains a function\. In this example, the Lambda function is created in another stack and is referenced using the `ImportValue` function\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-functiondefinitionversion-example1.json"></a>

```
"TestFunctionDefinition": {
    "Type": "AWS::Greengrass::FunctionDefinition",
    "Properties": {
        "Name": "DemoTestFunctionDefinition"
    }
},
"TestFunctionDefinitionVersion": {
    "Type": "AWS::Greengrass::FunctionDefinitionVersion",
    "Properties": {
        "FunctionDefinitionId": {
            "Fn::GetAtt": [
                "TestFunctionDefinition",
                "Id"
            ]
        },
        "DefaultConfig": {
            "Execution": {
                "IsolationMode": "GreengrassContainer"
            }
        },
        "Functions": [
            {
                "Id": "TestLambda1",
                "FunctionArn": {
                    "Fn::ImportValue": "TestCanaryLambdaVersionArn"
                },
                "FunctionConfiguration": {
                    "Pinned": "true",
                    "Executable": "run.exe",
                    "ExecArgs": "argument1",
                    "MemorySize": "512",
                    "Timeout": "2000",
                    "EncodingType": "binary",
                    "Environment": {
                        "Variables": {
                            "variable1": "value1"
                        },
                        "ResourceAccessPolicies": [
                            {
                                "ResourceId": "ResourceId1",
                                "Permission": "ro"
                            },
                            {
                                "ResourceId": "ResourceId2",
                                "Permission": "rw"
                            }
                        ],
                        "AccessSysfs": "false",
                        "Execution": {
                            "RunAs": {
                                "Uid": "1",
                                "Gid": "10"
                            }
                        }
                    }
                }
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-greengrass-functiondefinitionversion-example1.yaml"></a>

```
TestFunctionDefinition:
  Type: 'AWS::Greengrass::FunctionDefinition'
  Properties:
    Name: DemoTestFunctionDefinition
TestFunctionDefinitionVersion:
  Type: 'AWS::Greengrass::FunctionDefinitionVersion'
  Properties:
    FunctionDefinitionId: !GetAtt 
      - TestFunctionDefinition
      - Id
    DefaultConfig:
      Execution:
        IsolationMode: GreengrassContainer
    Functions:
      - Id: TestLambda1
        FunctionArn: !ImportValue TestCanaryLambdaVersionArn
        FunctionConfiguration:
          Pinned: 'true'
          Executable: run.exe
          ExecArgs: argument1
          MemorySize: '512'
          Timeout: '2000'
          EncodingType: binary
          Environment:
            Variables:
              variable1: value1
            ResourceAccessPolicies:
              - ResourceId: ResourceId1
                Permission: ro
              - ResourceId: ResourceId2
                Permission: rw
            AccessSysfs: 'false'
            Execution:
              RunAs:
                Uid: '1'
                Gid: '10'
```

## See Also<a name="aws-resource-greengrass-functiondefinitionversion-seealso"></a>
+ [FunctionDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functiondefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)