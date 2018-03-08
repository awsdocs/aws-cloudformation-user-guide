# Amazon S3 Bucket StorageClassAnalysis<a name="aws-properties-s3-bucket-storageclassanalysis"></a>

<a name="aws-properties-s3-bucket-storageclassanalysis-description"></a>The `StorageClassAnalysis` property type specifies data related to access patterns to be collected and made available to analyze the tradeoffs between different storage classes for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-storageclassanalysis-inheritance"></a> `StorageClassAnalysis` is a property of the [Amazon S3 Bucket AnalyticsConfiguration](aws-properties-s3-bucket-analyticsconfiguration.md) property type\. 

## Syntax<a name="aws-properties-s3-bucket-storageclassanalysis-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-storageclassanalysis-syntax.json"></a>

```
{
  "[DataExport](#cfn-s3-bucket-storageclassanalysis-dataexport)" : [*DataExport*](aws-properties-s3-bucket-dataexport.md)
}
```

### YAML<a name="aws-properties-s3-bucket-storageclassanalysis-syntax.yaml"></a>

```
[DataExport](#cfn-s3-bucket-storageclassanalysis-dataexport): DataExport
```

## Properties<a name="aws-properties-s3-bucket-storageclassanalysis-properties"></a>

`DataExport`  <a name="cfn-s3-bucket-storageclassanalysis-dataexport"></a>
Describes how data related to the storage class analysis should be exported\.  
 *Required*: No  
 *Type*: [Amazon S3 Bucket DataExport](aws-properties-s3-bucket-dataexport.md)   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 