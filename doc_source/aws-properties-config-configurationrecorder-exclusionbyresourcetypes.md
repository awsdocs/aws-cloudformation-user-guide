# AWS::Config::ConfigurationRecorder ExclusionByResourceTypes<a name="aws-properties-config-configurationrecorder-exclusionbyresourcetypes"></a>

Specifies whether the configuration recorder excludes resource types from being recorded\. Use the `resourceTypes` field to enter a comma\-separated list of resource types to exclude as exemptions\.

**Note**  
To use this option, you must set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `EXCLUSION_BY_RESOURCE_TYPES`\.

## Syntax<a name="aws-properties-config-configurationrecorder-exclusionbyresourcetypes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationrecorder-exclusionbyresourcetypes-syntax.json"></a>

```
{
  "[ResourceTypes](#cfn-config-configurationrecorder-exclusionbyresourcetypes-resourcetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-configurationrecorder-exclusionbyresourcetypes-syntax.yaml"></a>

```
  [ResourceTypes](#cfn-config-configurationrecorder-exclusionbyresourcetypes-resourcetypes): 
    - String
```

## Properties<a name="aws-properties-config-configurationrecorder-exclusionbyresourcetypes-properties"></a>

`ResourceTypes`  <a name="cfn-config-configurationrecorder-exclusionbyresourcetypes-resourcetypes"></a>
A comma\-separated list of resource types to exclude from recording by the configuration recorder\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)