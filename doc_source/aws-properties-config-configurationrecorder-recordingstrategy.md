# AWS::Config::ConfigurationRecorder RecordingStrategy<a name="aws-properties-config-configurationrecorder-recordingstrategy"></a>

Specifies the recording strategy of the configuration recorder\.

Valid values include: `ALL_SUPPORTED_RESOURCE_TYPES`, `INCLUSION_BY_RESOURCE_TYPES`, and `EXCLUSION_BY_RESOURCE_TYPES`\.

## Syntax<a name="aws-properties-config-configurationrecorder-recordingstrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationrecorder-recordingstrategy-syntax.json"></a>

```
{
  "[UseOnly](#cfn-config-configurationrecorder-recordingstrategy-useonly)" : String
}
```

### YAML<a name="aws-properties-config-configurationrecorder-recordingstrategy-syntax.yaml"></a>

```
  [UseOnly](#cfn-config-configurationrecorder-recordingstrategy-useonly): String
```

## Properties<a name="aws-properties-config-configurationrecorder-recordingstrategy-properties"></a>

`UseOnly`  <a name="cfn-config-configurationrecorder-recordingstrategy-useonly"></a>
The recording strategy for the configuration recorder\.  
+ If you set this option to `ALL_SUPPORTED_RESOURCE_TYPES`, AWS Config records configuration changes for all supported regionally recorded resource types\. You also must set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\. When AWS Config adds support for a new regionally recorded resource, AWS Config automatically starts recording resources of that type\. For a list of supported resource types, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the *AWS Config developer guide*\.
+ If you set this option to `INCLUSION_BY_RESOURCE_TYPES`, AWS Config records configuration changes for only the resource types that you specify in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-conew type of regional resourcenfigurationrecorder-recordinggroup.html)\.
+ If you set this option to `EXCLUSION_BY_RESOURCE_TYPES`, AWS Config records configuration changes for all supported resource types, except the resource types that you specify to exclude from being recorded in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
**Required and optional fields**  
The `recordingStrategy` field is optional when you set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\.  
The `recordingStrategy` field is optional when you list resource types in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html)\.  
The `recordingStrategy` field is required if you list resource types to exclude from recording in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
**Overriding fields**  
If you choose `EXCLUSION_BY_RESOURCE_TYPES` for the recording strategy, the `exclusionByResourceTypes` field will override other properties in the request\.  
For example, even if you set `includeGlobalResourceTypes` to false, global resource types will still be automatically recorded in this option unless those resource types are specifically listed as exclusions in the `resourceTypes` field of `exclusionByResourceTypes`\.
**Global resource types and the exclusion recording strategy**  
By default, if you choose the `EXCLUSION_BY_RESOURCE_TYPES` recording strategy, when AWS Config adds support for a new resource type in the Region where you set up the configuration recorder, including global resource types, AWS Config starts recording resources of that type automatically\.  
In addition, unless specifically listed as exclusions, `AWS::RDS::GlobalCluster` will be recorded automatically in all supported AWS Config Regions were the configuration recorder is enabled\. IAM users, groups, roles, and customer managed policies will be recorded automatically in all enabled AWS Config Regions where AWS Config was available before February 2022\. This list does not include the following Regions:  
+ Asia Pacific \(Hyderabad\)
+ Asia Pacific \(Melbourne\)
+ Europe \(Spain\)
+ Europe \(Zurich\)
+ Israel \(Tel Aviv\)
+ Middle East \(UAE\)
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)