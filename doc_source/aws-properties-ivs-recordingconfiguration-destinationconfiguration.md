# AWS::IVS::RecordingConfiguration DestinationConfiguration<a name="aws-properties-ivs-recordingconfiguration-destinationconfiguration"></a>

The DestinationConfiguration property type describes the location where recorded videos will be stored\. Each member represents a type of destination configuration\. For recording, you define one and only one type of destination configuration\.

## Syntax<a name="aws-properties-ivs-recordingconfiguration-destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivs-recordingconfiguration-destinationconfiguration-syntax.json"></a>

```
{
  "[S3](#cfn-ivs-recordingconfiguration-destinationconfiguration-s3)" : S3DestinationConfiguration
}
```

### YAML<a name="aws-properties-ivs-recordingconfiguration-destinationconfiguration-syntax.yaml"></a>

```
  [S3](#cfn-ivs-recordingconfiguration-destinationconfiguration-s3): 
    S3DestinationConfiguration
```

## Properties<a name="aws-properties-ivs-recordingconfiguration-destinationconfiguration-properties"></a>

`S3`  <a name="cfn-ivs-recordingconfiguration-destinationconfiguration-s3"></a>
An S3 destination configuration where recorded videos will be stored\. See the [S3DestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ivs-recordingconfiguration-s3destinationconfiguration.html) property type for more information\.  
*Required*: No  
*Type*: [S3DestinationConfiguration](aws-properties-ivs-recordingconfiguration-s3destinationconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)