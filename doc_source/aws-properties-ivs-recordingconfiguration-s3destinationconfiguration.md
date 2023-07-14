# AWS::IVS::RecordingConfiguration S3DestinationConfiguration<a name="aws-properties-ivs-recordingconfiguration-s3destinationconfiguration"></a>

The S3DestinationConfiguration property type describes an S3 location where recorded videos will be stored\.

## Syntax<a name="aws-properties-ivs-recordingconfiguration-s3destinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivs-recordingconfiguration-s3destinationconfiguration-syntax.json"></a>

```
{
  "[BucketName](#cfn-ivs-recordingconfiguration-s3destinationconfiguration-bucketname)" : String
}
```

### YAML<a name="aws-properties-ivs-recordingconfiguration-s3destinationconfiguration-syntax.yaml"></a>

```
  [BucketName](#cfn-ivs-recordingconfiguration-s3destinationconfiguration-bucketname): String
```

## Properties<a name="aws-properties-ivs-recordingconfiguration-s3destinationconfiguration-properties"></a>

`BucketName`  <a name="cfn-ivs-recordingconfiguration-s3destinationconfiguration-bucketname"></a>
Location \(S3 bucket name\) where recorded videos will be stored\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9-.]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)