# AWS::IoTAnalytics::Dataset GlueConfiguration<a name="aws-properties-iotanalytics-dataset-glueconfiguration"></a>

Configuration information for coordination with AWS Glue, a fully managed extract, transform and load \(ETL\) service\.

## Syntax<a name="aws-properties-iotanalytics-dataset-glueconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-glueconfiguration-syntax.json"></a>

```
{
  "[DatabaseName](#cfn-iotanalytics-dataset-glueconfiguration-databasename)" : String,
  "[TableName](#cfn-iotanalytics-dataset-glueconfiguration-tablename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-glueconfiguration-syntax.yaml"></a>

```
  [DatabaseName](#cfn-iotanalytics-dataset-glueconfiguration-databasename): String
  [TableName](#cfn-iotanalytics-dataset-glueconfiguration-tablename): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-glueconfiguration-properties"></a>

`DatabaseName`  <a name="cfn-iotanalytics-dataset-glueconfiguration-databasename"></a>
The name of the database in your AWS Glue Data Catalog in which the table is located\. An AWS Glue Data Catalog database contains metadata tables\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-iotanalytics-dataset-glueconfiguration-tablename"></a>
The name of the table in your AWS Glue Data Catalog that is used to perform the ETL operations\. An AWS Glue Data Catalog table contains partitioned data and descriptions of data sources and targets\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)