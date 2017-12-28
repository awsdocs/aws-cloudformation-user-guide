# AWS Config ConfigurationRecorder RecordingGroup<a name="aws-properties-config-configurationrecorder-recordinggroup"></a>

`RecordingGroup` is property of the [AWS::Config::ConfigurationRecorder](aws-resource-config-configurationrecorder.md) resource that defines which AWS resource types to include in a recording group\.

## Syntax<a name="w3ab2c21c14d464b5"></a>

### JSON<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-allsupported)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-resourcetypes)" : [ String, ... ]  
}
```

### YAML<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-allsupported): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-config-configurationrecorder-recordinggroup-resourcetypes):
  - String
```

## Properties<a name="w3ab2c21c14d464b7"></a>

`AllSupported`  
Indicates whether to record all supported resource types\. If you specify this property, do not specify the `ResourceTypes` property\.  
*Required: *No  
*Type*: Boolean

`IncludeGlobalResourceTypes`  
Indicates whether AWS Config records all supported global resource types\. When AWS Config supports new global resource types, AWS Config will automatically start recording them if you enable this property\.  
If you set this property to `true`, you must set the `AllSupported` property to `true`\.
*Required: *No  
*Type*: Boolean

`ResourceTypes`  
A list of valid AWS resource types to include in this recording group, such as **AWS::EC2::Instance** or **AWS::CloudTrail::Trail**\. If you specify this property, do not specify the `AllSupported` property\. For a list of supported resource types, see [Supported resource types](http://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the *AWS Config Developer Guide*\.  
*Required: *No  
*Type*: List of String values