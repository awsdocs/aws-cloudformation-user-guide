# AWS::DynamoDB::Table ImportSourceSpecification<a name="aws-properties-dynamodb-table-importsourcespecification"></a>

Specifies the properties of data being imported from the S3 bucket source to the table\.

## Syntax<a name="aws-properties-dynamodb-table-importsourcespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-importsourcespecification-syntax.json"></a>

```
{
  "[InputCompressionType](#cfn-dynamodb-table-importsourcespecification-inputcompressiontype)" : String,
  "[InputFormat](#cfn-dynamodb-table-importsourcespecification-inputformat)" : String,
  "[InputFormatOptions](#cfn-dynamodb-table-importsourcespecification-inputformatoptions)" : InputFormatOptions,
  "[S3BucketSource](#cfn-dynamodb-table-importsourcespecification-s3bucketsource)" : S3BucketSource
}
```

### YAML<a name="aws-properties-dynamodb-table-importsourcespecification-syntax.yaml"></a>

```
  [InputCompressionType](#cfn-dynamodb-table-importsourcespecification-inputcompressiontype): String
  [InputFormat](#cfn-dynamodb-table-importsourcespecification-inputformat): String
  [InputFormatOptions](#cfn-dynamodb-table-importsourcespecification-inputformatoptions): 
    InputFormatOptions
  [S3BucketSource](#cfn-dynamodb-table-importsourcespecification-s3bucketsource): 
    S3BucketSource
```

## Properties<a name="aws-properties-dynamodb-table-importsourcespecification-properties"></a>

`InputCompressionType`  <a name="cfn-dynamodb-table-importsourcespecification-inputcompressiontype"></a>
 Type of compression to be used on the input coming from the imported table\.   
*Required*: No  
*Type*: String  
*Allowed values*: `GZIP | NONE | ZSTD`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputFormat`  <a name="cfn-dynamodb-table-importsourcespecification-inputformat"></a>
 The format of the source data\. Valid values for `ImportFormat` are `CSV`, `DYNAMODB_JSON` or `ION`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `CSV | DYNAMODB_JSON | ION`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputFormatOptions`  <a name="cfn-dynamodb-table-importsourcespecification-inputformatoptions"></a>
 Additional properties that specify how the input is formatted,   
*Required*: No  
*Type*: [InputFormatOptions](aws-properties-dynamodb-table-inputformatoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3BucketSource`  <a name="cfn-dynamodb-table-importsourcespecification-s3bucketsource"></a>
 The S3 bucket that provides the source for the import\.   
*Required*: Yes  
*Type*: [S3BucketSource](aws-properties-dynamodb-table-s3bucketsource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)