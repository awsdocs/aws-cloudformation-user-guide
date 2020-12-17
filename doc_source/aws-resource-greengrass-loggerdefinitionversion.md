# AWS::Greengrass::LoggerDefinitionVersion<a name="aws-resource-greengrass-loggerdefinitionversion"></a>

The `AWS::Greengrass::LoggerDefinitionVersion` resource represents a logger definition version for AWS IoT Greengrass\. A logger definition version contains a list of loggers\.

**Note**  
To create a logger definition version, you must specify the ID of the logger definition that you want to associate with the version\. For information about creating a logger definition, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)\.  
After you create a logger definition version that contains the loggers you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-loggerdefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-loggerdefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::LoggerDefinitionVersion",
  "Properties" : {
      "[LoggerDefinitionId](#cfn-greengrass-loggerdefinitionversion-loggerdefinitionid)" : String,
      "[Loggers](#cfn-greengrass-loggerdefinitionversion-loggers)" : [ Logger, ... ]
    }
}
```

### YAML<a name="aws-resource-greengrass-loggerdefinitionversion-syntax.yaml"></a>

```
Type: AWS::Greengrass::LoggerDefinitionVersion
Properties: 
  [LoggerDefinitionId](#cfn-greengrass-loggerdefinitionversion-loggerdefinitionid): String
  [Loggers](#cfn-greengrass-loggerdefinitionversion-loggers): 
    - Logger
```

## Properties<a name="aws-resource-greengrass-loggerdefinitionversion-properties"></a>

`LoggerDefinitionId`  <a name="cfn-greengrass-loggerdefinitionversion-loggerdefinitionid"></a>
The ID of the logger definition associated with this version\. This value is a GUID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Loggers`  <a name="cfn-greengrass-loggerdefinitionversion-loggers"></a>
The loggers in this version\.  
*Required*: Yes  
*Type*: List of [Logger](aws-properties-greengrass-loggerdefinitionversion-logger.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-greengrass-loggerdefinitionversion-return-values"></a>

### Ref<a name="aws-resource-greengrass-loggerdefinitionversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the logger definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-greengrass-loggerdefinitionversion--examples"></a>



### Logger Definition Version Snippet<a name="aws-resource-greengrass-loggerdefinitionversion--examples--Logger_Definition_Version_Snippet"></a>

The following snippet defines logger definition and logger definition version resources\. The logger definition version references the logger definition and contains a logger\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-loggerdefinitionversion--examples--Logger_Definition_Version_Snippet--json"></a>

```
"TestLoggerDefinition": {
    "Type": "AWS::Greengrass::LoggerDefinition",
    "Properties": {
        "Name": "DemoTestLoggerDefinition"
    }
},
"TestLoggerDefinitionVersion": {
    "Type": "AWS::Greengrass::LoggerDefinitionVersion",
    "Properties": {
        "LoggerDefinitionId": {
            "Ref": "TestLoggerDefinition"
        },
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
```

#### YAML<a name="aws-resource-greengrass-loggerdefinitionversion--examples--Logger_Definition_Version_Snippet--yaml"></a>

```
TestLoggerDefinition:
  Type: 'AWS::Greengrass::LoggerDefinition'
  Properties:
    Name: DemoTestLoggerDefinition
TestLoggerDefinitionVersion:
  Type: 'AWS::Greengrass::LoggerDefinitionVersion'
  Properties:
    LoggerDefinitionId: !Ref TestLoggerDefinition
    Loggers:
      - Id: TestLogger1
        Type: FileSystem
        Component: GreengrassSystem
        Level: INFO
        Space: '128'
```

## See also<a name="aws-resource-greengrass-loggerdefinitionversion--seealso"></a>
+  [CreateLoggerDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/createloggerdefinitionversion-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 