# AWS::Greengrass::LoggerDefinition<a name="aws-resource-greengrass-loggerdefinition"></a>

The `AWS::Greengrass::LoggerDefinition` resource represents a logger definition for AWS IoT Greengrass\. Logger definitions are used to organize your logger definition versions\.

Logger definitions can reference multiple logger definition versions\. All logger definition versions must be associated with a logger definition\. Each logger definition version can contain one or more loggers\.

**Note**  
When you create a logger definition, you can optionally include an initial logger definition version\. To associate a logger definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinitionversion.html) resource and specify the ID of this logger definition\.  
After you create the logger definition version that contains the loggers you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-loggerdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-loggerdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::LoggerDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-loggerdefinition-initialversion)" : LoggerDefinitionVersion,
      "[Name](#cfn-greengrass-loggerdefinition-name)" : String,
      "[Tags](#cfn-greengrass-loggerdefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-loggerdefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::LoggerDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-loggerdefinition-initialversion): 
    LoggerDefinitionVersion
  [Name](#cfn-greengrass-loggerdefinition-name): String
  [Tags](#cfn-greengrass-loggerdefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-loggerdefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-loggerdefinition-initialversion"></a>
The logger definition version to include when the logger definition is created\. A logger definition version contains a list of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-loggerdefinition-logger.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-loggerdefinition-logger.html) property types\.  
To associate a logger definition version after the logger definition is created, create an [ `AWS::Greengrass::LoggerDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinitionversion.html) resource and specify the ID of this logger definition\.
*Required*: No  
*Type*: [LoggerDefinitionVersion](aws-properties-greengrass-loggerdefinition-loggerdefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-loggerdefinition-name"></a>
The name of the logger definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-loggerdefinition-tags"></a>
Application\-specific metadata to attach to the logger definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
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

## Return values<a name="aws-resource-greengrass-loggerdefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-loggerdefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the logger definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-loggerdefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-loggerdefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `LoggerDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `LoggerDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `LoggerDefinitionVersion` that was added to the `LoggerDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `LoggerDefinition`, such as `MyLoggerDefinition`\. 

## Examples<a name="aws-resource-greengrass-loggerdefinition--examples"></a>



### Logger Definition Snippet<a name="aws-resource-greengrass-loggerdefinition--examples--Logger_Definition_Snippet"></a>

The following snippet defines a logger definition resource with an initial version that contains a logger\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-loggerdefinition--examples--Logger_Definition_Snippet--json"></a>

```
"TestLoggerDefinition": {
    "Type": "AWS::Greengrass::LoggerDefinition",
    "Properties": {
        "Name": "DemoTestLoggerDefinition",
        "InitialVersion": {
            "Loggers": [
                {
                    "Id": "TestLogger1",
                    "Type": "FileSystem",
                    "Component": "GreengrassSystem",
                    "Level": "INFO",
                    "Space": "128"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-loggerdefinition--examples--Logger_Definition_Snippet--yaml"></a>

```
TestLoggerDefinition:
  Type: 'AWS::Greengrass::LoggerDefinition'
  Properties:
    Name: DemoTestLoggerDefinition
    InitialVersion:
      Loggers:
        - Id: TestLogger1
          Type: FileSystem
          Component: GreengrassSystem
          Level: INFO
          Space: '128'
```

## See also<a name="aws-resource-greengrass-loggerdefinition--seealso"></a>
+  [CreateLoggerDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createloggerdefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 