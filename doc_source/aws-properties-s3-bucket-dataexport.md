# Amazon S3 Bucket DataExport<a name="aws-properties-s3-bucket-dataexport"></a>

<a name="aws-properties-s3-bucket-dataexport-description"></a>The `DataExport` property type specifies how data related to the storage class analysis should be exported for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-dataexport-inheritance"></a> `DataExport` is a property of the [Amazon S3 Bucket StorageClassAnalysis](aws-properties-s3-bucket-storageclassanalysis.md) property type\. 

## Syntax<a name="aws-properties-s3-bucket-dataexport-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-dataexport-syntax.json"></a>

```
{
  "[Destination](#cfn-s3-bucket-dataexport-destination)" : [*Destination*](aws-properties-s3-bucket-destination.md),
  "[OutputSchemaVersion](#cfn-s3-bucket-dataexport-outputschemaversion)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-dataexport-syntax.yaml"></a>

```
[Destination](#cfn-s3-bucket-dataexport-destination): Destination
[OutputSchemaVersion](#cfn-s3-bucket-dataexport-outputschemaversion): String
```

## Properties<a name="aws-properties-s3-bucket-dataexport-properties"></a>

`Destination`  <a name="cfn-s3-bucket-dataexport-destination"></a>
Information about where to publish the analytics results\.  
 *Required*: Yes  
 *Type*: [Amazon S3 Bucket Destination](aws-properties-s3-bucket-destination.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OutputSchemaVersion`  <a name="cfn-s3-bucket-dataexport-outputschemaversion"></a>
The version of the output schema to use when exporting data\. Must be V\_1\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 