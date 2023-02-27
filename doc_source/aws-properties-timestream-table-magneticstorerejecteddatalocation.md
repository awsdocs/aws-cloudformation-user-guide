# AWS::Timestream::Table MagneticStoreRejectedDataLocation<a name="aws-properties-timestream-table-magneticstorerejecteddatalocation"></a>

The location to write error reports for records rejected, asynchronously, during magnetic store writes\.

## Syntax<a name="aws-properties-timestream-table-magneticstorerejecteddatalocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-table-magneticstorerejecteddatalocation-syntax.json"></a>

```
{
  "[S3Configuration](#cfn-timestream-table-magneticstorerejecteddatalocation-s3configuration)" : S3Configuration
}
```

### YAML<a name="aws-properties-timestream-table-magneticstorerejecteddatalocation-syntax.yaml"></a>

```
  [S3Configuration](#cfn-timestream-table-magneticstorerejecteddatalocation-s3configuration): 
    S3Configuration
```

## Properties<a name="aws-properties-timestream-table-magneticstorerejecteddatalocation-properties"></a>

`S3Configuration`  <a name="cfn-timestream-table-magneticstorerejecteddatalocation-s3configuration"></a>
Configuration of an S3 location to write error reports for records rejected, asynchronously, during magnetic store writes\.  
*Required*: No  
*Type*: [S3Configuration](aws-properties-timestream-table-s3configuration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)