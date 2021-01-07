# AWS::Greengrass::FunctionDefinitionVersion<a name="aws-resource-greengrass-functiondefinitionversion"></a>

The `AWS::Greengrass::FunctionDefinitionVersion` resource represents a function definition version for AWS IoT Greengrass\. A function definition version contains contain a list of functions\.

**Note**  
To create a function definition version, you must specify the ID of the function definition that you want to associate with the version\. For information about creating a function definition, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html)\.  
After you create a function definition version that contains the functions you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-functiondefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-functiondefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::FunctionDefinitionVersion",
  "Properties" : {
      "[DefaultConfig](#cfn-greengrass-functiondefinitionversion-defaultconfig)" : DefaultConfig,
      "[FunctionDefinitionId](#cfn-greengrass-functiondefinitionversion-functiondefinitionid)" : String,
      "[Functions](#cfn-greengrass-functiondefinitionversion-functions)" : [ Function, ... ]
    }
}
```

### YAML<a name="aws-resource-greengrass-functiondefinitionversion-syntax.yaml"></a>

```
Type: AWS::Greengrass::FunctionDefinitionVersion
Properties: 
  [DefaultConfig](#cfn-greengrass-functiondefinitionversion-defaultconfig): 
    DefaultConfig
  [FunctionDefinitionId](#cfn-greengrass-functiondefinitionversion-functiondefinitionid): String
  [Functions](#cfn-greengrass-functiondefinitionversion-functions): 
    - Function
```

## Properties<a name="aws-resource-greengrass-functiondefinitionversion-properties"></a>

`DefaultConfig`  <a name="cfn-greengrass-functiondefinitionversion-defaultconfig"></a>
The default configuration that applies to all Lambda functions in the group\. Individual Lambda functions can override these settings\.  
*Required*: No  
*Type*: [DefaultConfig](aws-properties-greengrass-functiondefinitionversion-defaultconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FunctionDefinitionId`  <a name="cfn-greengrass-functiondefinitionversion-functiondefinitionid"></a>
The ID of the function definition associated with this version\. This value is a GUID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Functions`  <a name="cfn-greengrass-functiondefinitionversion-functions"></a>
The functions in this version\.  
*Required*: Yes  
*Type*: List of [Function](aws-properties-greengrass-functiondefinitionversion-function.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrass-functiondefinitionversion-return-values"></a>

### Ref<a name="aws-resource-greengrass-functiondefinitionversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the function definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-greengrass-functiondefinitionversion--examples"></a>



### Function Definition Version Snippet<a name="aws-resource-greengrass-functiondefinitionversion--examples--Function_Definition_Version_Snippet"></a>

The following snippet defines function definition and function definition version resources\. The function definition version references the function definition and contains a function\. In this example, the Lambda function is created in another stack and is referenced using the `ImportValue` function\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-functiondefinitionversion--examples--Function_Definition_Version_Snippet--json"></a>

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

#### YAML<a name="aws-resource-greengrass-functiondefinitionversion--examples--Function_Definition_Version_Snippet--yaml"></a>

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

## See also<a name="aws-resource-greengrass-functiondefinitionversion--seealso"></a>
+  [CreateFunctionDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/createfunctiondefinitionversion-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 