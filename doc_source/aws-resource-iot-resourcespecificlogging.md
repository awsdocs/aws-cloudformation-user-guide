# AWS::IoT::ResourceSpecificLogging<a name="aws-resource-iot-resourcespecificlogging"></a>

Sets the logging options for a specific resource in the V2 logging service\.

## Syntax<a name="aws-resource-iot-resourcespecificlogging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-resourcespecificlogging-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::ResourceSpecificLogging",
  "Properties" : {
      "[LogLevel](#cfn-iot-resourcespecificlogging-loglevel)" : String,
      "[TargetName](#cfn-iot-resourcespecificlogging-targetname)" : String,
      "[TargetType](#cfn-iot-resourcespecificlogging-targettype)" : String
    }
}
```

### YAML<a name="aws-resource-iot-resourcespecificlogging-syntax.yaml"></a>

```
Type: AWS::IoT::ResourceSpecificLogging
Properties: 
  [LogLevel](#cfn-iot-resourcespecificlogging-loglevel): String
  [TargetName](#cfn-iot-resourcespecificlogging-targetname): String
  [TargetType](#cfn-iot-resourcespecificlogging-targettype): String
```

## Properties<a name="aws-resource-iot-resourcespecificlogging-properties"></a>

`LogLevel`  <a name="cfn-iot-resourcespecificlogging-loglevel"></a>
The logging level\. Valid values are `DEBUG`, `INFO`, `ERROR`, `WARN`, and `DISABLED`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetName`  <a name="cfn-iot-resourcespecificlogging-targetname"></a>
The log target name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetType`  <a name="cfn-iot-resourcespecificlogging-targettype"></a>
The log target type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-resourcespecificlogging-return-values"></a>

### Ref<a name="aws-resource-iot-resourcespecificlogging-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns

 `{ "Ref": "TargetType:TargetName" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-resourcespecificlogging-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-resourcespecificlogging-return-values-fn--getatt-fn--getatt"></a>

`TargetId`  <a name="TargetId-fn::getatt"></a>
The unique identifier of the log target\.