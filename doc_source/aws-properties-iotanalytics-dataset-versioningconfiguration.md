# AWS::IoTAnalytics::Dataset VersioningConfiguration<a name="aws-properties-iotanalytics-dataset-versioningconfiguration"></a>

Information about the versioning of data set contents\.

## Syntax<a name="aws-properties-iotanalytics-dataset-versioningconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-versioningconfiguration-syntax.json"></a>

```
{
  "[MaxVersions](#cfn-iotanalytics-dataset-versioningconfiguration-maxversions)" : Integer,
  "[Unlimited](#cfn-iotanalytics-dataset-versioningconfiguration-unlimited)" : Boolean
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-versioningconfiguration-syntax.yaml"></a>

```
  [MaxVersions](#cfn-iotanalytics-dataset-versioningconfiguration-maxversions): Integer
  [Unlimited](#cfn-iotanalytics-dataset-versioningconfiguration-unlimited): Boolean
```

## Properties<a name="aws-properties-iotanalytics-dataset-versioningconfiguration-properties"></a>

`MaxVersions`  <a name="cfn-iotanalytics-dataset-versioningconfiguration-maxversions"></a>
How many versions of data set contents will be kept\. The "unlimited" parameter must be false\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unlimited`  <a name="cfn-iotanalytics-dataset-versioningconfiguration-unlimited"></a>
If true, unlimited versions of data set contents will be kept\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
