# AWS::Greengrass::FunctionDefinition<a name="aws-resource-greengrass-functiondefinition"></a>

The `AWS::Greengrass::FunctionDefinition` resource represents a function definition for AWS IoT Greengrass\. Function definitions are used to organize your function definition versions\.

Function definitions can reference multiple function definition versions\. All function definition versions must be associated with a function definition\. Each function definition version can contain one or more functions\.

**Note**  
When you create a function definition, you can optionally include an initial function definition version\. To associate a function definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html) resource and specify the ID of this function definition\.  
After you create the function definition version that contains the functions you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-functiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-functiondefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::FunctionDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-functiondefinition-initialversion)" : FunctionDefinitionVersion,
      "[Name](#cfn-greengrass-functiondefinition-name)" : String,
      "[Tags](#cfn-greengrass-functiondefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-functiondefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::FunctionDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-functiondefinition-initialversion): 
    FunctionDefinitionVersion
  [Name](#cfn-greengrass-functiondefinition-name): String
  [Tags](#cfn-greengrass-functiondefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-functiondefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-functiondefinition-initialversion"></a>
The function definition version to include when the function definition is created\. A function definition version contains a list of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-function.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-function.html) property types\.  
To associate a function definition version after the function definition is created, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html) resource and specify the ID of this function definition\.
*Required*: No  
*Type*: [FunctionDefinitionVersion](aws-properties-greengrass-functiondefinition-functiondefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-functiondefinition-name"></a>
The name of the function definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-functiondefinition-tags"></a>
Application\-specific metadata to attach to the function definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
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

## Return values<a name="aws-resource-greengrass-functiondefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-functiondefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the function definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-functiondefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-functiondefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `FunctionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `FunctionDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `FunctionDefinitionVersion` that was added to the `FunctionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `FunctionDefinition`, such as `MyFunctionDefinition`\. 

## Examples<a name="aws-resource-greengrass-functiondefinition--examples"></a>



### Function Definition Snippet<a name="aws-resource-greengrass-functiondefinition--examples--Function_Definition_Snippet"></a>

The following snippet defines a function definition resource with an initial version that contains a function\. In this example, the Lambda function is created in another stack and is referenced using the `ImportValue` function\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-functiondefinition--examples--Function_Definition_Snippet--json"></a>

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

#### YAML<a name="aws-resource-greengrass-functiondefinition--examples--Function_Definition_Snippet--yaml"></a>

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

## See also<a name="aws-resource-greengrass-functiondefinition--seealso"></a>
+  [CreateFunctionDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createfunctiondefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 