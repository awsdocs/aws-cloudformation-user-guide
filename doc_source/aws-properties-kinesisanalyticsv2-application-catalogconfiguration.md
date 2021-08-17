# AWS::KinesisAnalyticsV2::Application CatalogConfiguration<a name="aws-properties-kinesisanalyticsv2-application-catalogconfiguration"></a>

The configuration parameters for the default Amazon Glue database\. You use this database for SQL queries that you write in a Kinesis Data Analytics Studio notebook\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-catalogconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-catalogconfiguration-syntax.json"></a>

```
{
  "[GlueDataCatalogConfiguration](#cfn-kinesisanalyticsv2-application-catalogconfiguration-gluedatacatalogconfiguration)" : GlueDataCatalogConfiguration
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-catalogconfiguration-syntax.yaml"></a>

```
  [GlueDataCatalogConfiguration](#cfn-kinesisanalyticsv2-application-catalogconfiguration-gluedatacatalogconfiguration): 
    GlueDataCatalogConfiguration
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-catalogconfiguration-properties"></a>

`GlueDataCatalogConfiguration`  <a name="cfn-kinesisanalyticsv2-application-catalogconfiguration-gluedatacatalogconfiguration"></a>
The configuration parameters for the default Amazon Glue database\. You use this database for Apache Flink SQL queries and table API transforms that you write in a Kinesis Data Analytics Studio notebook\.  
*Required*: No  
*Type*: [GlueDataCatalogConfiguration](aws-properties-kinesisanalyticsv2-application-gluedatacatalogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)