# Amazon S3 Bucket DataExport<a name="aws-properties-s3-bucket-dataexport"></a>

<a name="aws-properties-s3-bucket-dataexport-description"></a>The `DataExport` property type specifies how data related to the storage class analysis should be exported for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-dataexport-inheritance"></a> `DataExport` is a property of the [Amazon S3 Bucket StorageClassAnalysis](aws-properties-s3-bucket-storageclassanalysis.md) property type\. 

## Syntax<a name="aws-properties-s3-bucket-dataexport-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-dataexport-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-dataexport-destination)" : Destination,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-dataexport-outputschemaversion)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-dataexport-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-dataexport-destination): Destination
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-dataexport-outputschemaversion): String
```

## Properties<a name="aws-properties-s3-bucket-dataexport-properties"></a>

`Destination`  
Information about where to publish the analytics results\.  
 *Required*: Yes  
 *Type*: [Amazon S3 Bucket Destination](aws-properties-s3-bucket-destination.md)  
 *Update requires*: No interruption 

`OutputSchemaVersion`  
The version of the output schema to use when exporting data\. Must be V\_1\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 