# AWS::KinesisAnalytics::ApplicationReferenceDataSource JSONMappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters"></a>

Provides additional mapping information when JSON is the record format on the streaming source\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax.yaml"></a>

```
  [RecordRowPath](#cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath"></a>
Path to the top\-level parent that contains the records\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
