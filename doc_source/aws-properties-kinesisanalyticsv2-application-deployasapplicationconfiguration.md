# AWS::KinesisAnalyticsV2::Application DeployAsApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-deployasapplicationconfiguration"></a>

The information required to deploy a Kinesis Data Analytics Studio notebook as an application with durable state\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-deployasapplicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-deployasapplicationconfiguration-syntax.json"></a>

```
{
  "[S3ContentLocation](#cfn-kinesisanalyticsv2-application-deployasapplicationconfiguration-s3contentlocation)" : S3ContentBaseLocation
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-deployasapplicationconfiguration-syntax.yaml"></a>

```
  [S3ContentLocation](#cfn-kinesisanalyticsv2-application-deployasapplicationconfiguration-s3contentlocation): 
    S3ContentBaseLocation
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-deployasapplicationconfiguration-properties"></a>

`S3ContentLocation`  <a name="cfn-kinesisanalyticsv2-application-deployasapplicationconfiguration-s3contentlocation"></a>
The description of an Amazon S3 object that contains the Amazon Data Analytics application, including the Amazon Resource Name \(ARN\) of the S3 bucket, the name of the Amazon S3 object that contains the data, and the version number of the Amazon S3 object that contains the data\.   
*Required*: Yes  
*Type*: [S3ContentBaseLocation](aws-properties-kinesisanalyticsv2-application-s3contentbaselocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)