# AWS::Greengrass::FunctionDefinition<a name="aws-resource-greengrass-functiondefinition"></a>

The `AWS::Greengrass::FunctionDefinition` resource represents a function definition for AWS IoT Greengrass\. Function definitions are used to organize your function definition versions\.

Function definitions can reference multiple function definition versions\.

![\[A function definition hierarchy with associated function definition versions and functions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-function.png)

All function definition versions must be associated with a function definition\. Each function definition version can contain one or more functions\.

**Note**  
When you create a function definition, you can optionally include an initial function definition version\. To associate a function definition version later, create an [AWS::Greengrass::FunctionDefinitionVersion](aws-resource-greengrass-functiondefinitionversion.md) resource and specify the ID of this function definition\.  
After you create the function definition version that contains the functions you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-functiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-functiondefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::FunctionDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-functiondefinition-initialversion)" : [*FunctionDefinitionVersion*](aws-properties-greengrass-functiondefinition-functiondefinitionversion.md),
    "[Name](#cfn-greengrass-functiondefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-functiondefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::FunctionDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-functiondefinition-initialversion): 
    [*FunctionDefinitionVersion*](aws-properties-greengrass-functiondefinition-functiondefinitionversion.md)
  [Name](#cfn-greengrass-functiondefinition-name): String
```

## Properties<a name="aws-resource-greengrass-functiondefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-functiondefinition-initialversion"></a>
The function definition version to include when the function definition is created\. A function definition version contains a list of [`function`](aws-properties-greengrass-functiondefinition-function.md) property types\.  
To associate a function definition version after the function definition is created, create an [AWS::Greengrass::FunctionDefinitionVersion](aws-resource-greengrass-functiondefinitionversion.md) resource and specify the ID of this function definition\.
 *Required*: No  
 *Type*: [FunctionDefinitionVersion](aws-properties-greengrass-functiondefinition-functiondefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-functiondefinition-name"></a>
The name of the function definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-functiondefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-functiondefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::FunctionDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the function definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-functiondefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `FunctionDefinitionVersion` that was added to the `FunctionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `FunctionDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `FunctionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `FunctionDefinition`, such as `MyFunctionDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-functiondefinition-examples"></a>

### Function Definition Snippet<a name="aws-resource-greengrass-functiondefinition-example1"></a>

The following snippet defines a function definition resource with an initial version that contains a function\. In this example, the Lambda function is created in another stack and is referenced using the `ImportValue` function\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-functiondefinition-example1.json"></a>

```
"TestFunctionDefinition": {
    "Type": "AWS::Greengrass::FunctionDefinition",
    "Properties": {
        "Name": "DemoTestFunctionDefinition",
        "InitialVersion": {
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
                        "Pinned": "false",
                        "Executable": "run.exe",
                        "ExecArgs": "argument1",
                        "MemorySize": "256",
                        "Timeout": "3000",
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
                            "AccessSysfs": "true",
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
}
```

#### YAML<a name="aws-resource-greengrass-functiondefinition-example1.yaml"></a>

```
TestFunctionDefinition:
  Type: 'AWS::Greengrass::FunctionDefinition'
  Properties:
    Name: DemoTestFunctionDefinition
    InitialVersion:
      DefaultConfig:
        Execution:
          IsolationMode: GreengrassContainer
      Functions:
        - Id: TestLambda1
          FunctionArn: !ImportValue TestCanaryLambdaVersionArn
          FunctionConfiguration:
            Pinned: 'false'
            Executable: run.exe
            ExecArgs: argument1
            MemorySize: '256'
            Timeout: '3000'
            EncodingType: binary
            Environment:
              Variables:
                variable1: value1
              ResourceAccessPolicies:
                - ResourceId: ResourceId1
                  Permission: ro
                - ResourceId: ResourceId2
                  Permission: rw
              AccessSysfs: 'true'
              Execution:
                RunAs:
                  Uid: '1'
                  Gid: '10'
```

## See Also<a name="aws-resource-greengrass-functiondefinition-seealso"></a>
+ [CreateFunctionDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createfunctiondefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)