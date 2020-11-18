# AWS::S3::Bucket IntelligentTieringConfiguration<a name="aws-properties-s3-bucket-intelligenttieringconfiguration"></a>

Specifies the S3 Intelligent\-Tiering configuration for an Amazon S3 bucket\.

For information about the S3 Intelligent\-Tiering storage class, see [Storage class for automatically optimizing frequently and infrequently accessed objects](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html#sc-dynamic-data-access)\.

## Syntax<a name="aws-properties-s3-bucket-intelligenttieringconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-intelligenttieringconfiguration-syntax.json"></a>

```
{
  "[Id](#cfn-s3-bucket-intelligenttieringconfiguration-id)" : String,
  "[Prefix](#cfn-s3-bucket-intelligenttieringconfiguration-prefix)" : String,
  "[Status](#cfn-s3-bucket-intelligenttieringconfiguration-status)" : String,
  "[TagFilters](#cfn-s3-bucket-intelligenttieringconfiguration-tagfilters)" : [ TagFilter, ... ],
  "[Tierings](#cfn-s3-bucket-intelligenttieringconfiguration-tierings)" : [ Tiering, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-intelligenttieringconfiguration-syntax.yaml"></a>

```
  [Id](#cfn-s3-bucket-intelligenttieringconfiguration-id): String
  [Prefix](#cfn-s3-bucket-intelligenttieringconfiguration-prefix): String
  [Status](#cfn-s3-bucket-intelligenttieringconfiguration-status): String
  [TagFilters](#cfn-s3-bucket-intelligenttieringconfiguration-tagfilters): 
    - TagFilter
  [Tierings](#cfn-s3-bucket-intelligenttieringconfiguration-tierings): 
    - Tiering
```

## Properties<a name="aws-properties-s3-bucket-intelligenttieringconfiguration-properties"></a>

`Id`  <a name="cfn-s3-bucket-intelligenttieringconfiguration-id"></a>
The ID used to identify the S3 Intelligent\-Tiering configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-intelligenttieringconfiguration-prefix"></a>
An object key name prefix that identifies the subset of objects to which the rule applies\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-s3-bucket-intelligenttieringconfiguration-status"></a>
Specifies the status of the configuration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-s3-bucket-intelligenttieringconfiguration-tagfilters"></a>
A container for a key\-value pair\.  
*Required*: No  
*Type*: List of [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tierings`  <a name="cfn-s3-bucket-intelligenttieringconfiguration-tierings"></a>
Specifies the S3 Intelligent\-Tiering storage class tier of the configuration\.  
*Required*: Yes  
*Type*: List of [Tiering](aws-properties-s3-bucket-tiering.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)