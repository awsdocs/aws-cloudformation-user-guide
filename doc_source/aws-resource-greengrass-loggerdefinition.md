# AWS::Greengrass::LoggerDefinition<a name="aws-resource-greengrass-loggerdefinition"></a>

The `AWS::Greengrass::LoggerDefinition` resource represents a logger definition for AWS IoT Greengrass\. Logger definitions are used to organize your logger definition versions\.

Logger definitions can reference multiple logger definition versions\.

![\[A logger definition hierarchy with associated logger definition versions and loggers.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-logger.png)

All logger definition versions must be associated with a logger definition\. Each logger definition version can contain one or more loggers\.

**Note**  
When you create a logger definition, you can optionally include an initial logger definition version\. To associate a logger definition version later, create an [AWS::Greengrass::LoggerDefinitionVersion](aws-resource-greengrass-loggerdefinitionversion.md) resource and specify the ID of this logger definition\.  
After you create the logger definition version that contains the loggers you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-loggerdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-loggerdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::LoggerDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-loggerdefinition-initialversion)" : [*LoggerDefinitionVersion*](aws-properties-greengrass-loggerdefinition-loggerdefinitionversion.md),
    "[Name](#cfn-greengrass-loggerdefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-loggerdefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::LoggerDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-loggerdefinition-initialversion): 
    [*LoggerDefinitionVersion*](aws-properties-greengrass-loggerdefinition-loggerdefinitionversion.md)
  [Name](#cfn-greengrass-loggerdefinition-name): String
```

## Properties<a name="aws-resource-greengrass-loggerdefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-loggerdefinition-initialversion"></a>
The logger definition version to include when the logger definition is created\. A logger definition version contains a list of [`logger`](aws-properties-greengrass-loggerdefinition-logger.md) property types\.  
To associate a logger definition version after the logger definition is created, create an [AWS::Greengrass::LoggerDefinitionVersion](aws-resource-greengrass-loggerdefinitionversion.md) resource and specify the ID of this logger definition\.
 *Required*: No  
 *Type*: [LoggerDefinitionVersion](aws-properties-greengrass-loggerdefinition-loggerdefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-loggerdefinition-name"></a>
The name of the logger definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-loggerdefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-loggerdefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::LoggerDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the logger definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-loggerdefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `LoggerDefinitionVersion` that was added to the `LoggerDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `LoggerDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `LoggerDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `LoggerDefinition`, such as `MyLoggerDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-loggerdefinition-examples"></a>

### Logger Definition Snippet<a name="aws-resource-greengrass-loggerdefinition-example1"></a>

The following snippet defines a logger definition resource with an initial version that contains a logger\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-loggerdefinition-example1.json"></a>

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

#### YAML<a name="aws-resource-greengrass-loggerdefinition-example1.yaml"></a>

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

## See Also<a name="aws-resource-greengrass-loggerdefinition-seealso"></a>
+ [CreateLoggerDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createloggerdefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)