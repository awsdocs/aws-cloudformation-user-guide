# AWS::S3::Bucket DataExport<a name="aws-properties-s3-bucket-dataexport"></a>

Specifies how data related to the storage class analysis for an Amazon S3 bucket should be exported\.

## Syntax<a name="aws-properties-s3-bucket-dataexport-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-dataexport-syntax.json"></a>

```
{
  "[Destination](#cfn-s3-bucket-dataexport-destination)" : Destination,
  "[OutputSchemaVersion](#cfn-s3-bucket-dataexport-outputschemaversion)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-dataexport-syntax.yaml"></a>

```
  [Destination](#cfn-s3-bucket-dataexport-destination): 
    Destination
  [OutputSchemaVersion](#cfn-s3-bucket-dataexport-outputschemaversion): String
```

## Properties<a name="aws-properties-s3-bucket-dataexport-properties"></a>

`Destination`  <a name="cfn-s3-bucket-dataexport-destination"></a>
The place to store the data for an analysis\.  
*Required*: Yes  
*Type*: [Destination](aws-properties-s3-bucket-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSchemaVersion`  <a name="cfn-s3-bucket-dataexport-outputschemaversion"></a>
The version of the output schema to use when exporting data\. Must be `V_1`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `V_1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-dataexport--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

