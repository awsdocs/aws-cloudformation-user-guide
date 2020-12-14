# AWS::S3::StorageLens StorageLensConfiguration<a name="aws-properties-s3-storagelens-storagelensconfiguration"></a>

This is the property of the Amazon S3 Storage Lens configuration\.

## Syntax<a name="aws-properties-s3-storagelens-storagelensconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-storagelensconfiguration-syntax.json"></a>

```
{
  "[AccountLevel](#cfn-s3-storagelens-storagelensconfiguration-accountlevel)" : AccountLevel,
  "[AwsOrg](#cfn-s3-storagelens-storagelensconfiguration-awsorg)" : AwsOrg,
  "[DataExport](#cfn-s3-storagelens-storagelensconfiguration-dataexport)" : DataExport,
  "[Exclude](#cfn-s3-storagelens-storagelensconfiguration-exclude)" : BucketsAndRegions,
  "[Id](#cfn-s3-storagelens-storagelensconfiguration-id)" : String,
  "[Include](#cfn-s3-storagelens-storagelensconfiguration-include)" : BucketsAndRegions,
  "[IsEnabled](#cfn-s3-storagelens-storagelensconfiguration-isenabled)" : Boolean,
  "[StorageLensArn](#cfn-s3-storagelens-storagelensconfiguration-storagelensarn)" : String
}
```

### YAML<a name="aws-properties-s3-storagelens-storagelensconfiguration-syntax.yaml"></a>

```
  [AccountLevel](#cfn-s3-storagelens-storagelensconfiguration-accountlevel): 
    AccountLevel
  [AwsOrg](#cfn-s3-storagelens-storagelensconfiguration-awsorg): 
    AwsOrg
  [DataExport](#cfn-s3-storagelens-storagelensconfiguration-dataexport): 
    DataExport
  [Exclude](#cfn-s3-storagelens-storagelensconfiguration-exclude): 
    BucketsAndRegions
  [Id](#cfn-s3-storagelens-storagelensconfiguration-id): String
  [Include](#cfn-s3-storagelens-storagelensconfiguration-include): 
    BucketsAndRegions
  [IsEnabled](#cfn-s3-storagelens-storagelensconfiguration-isenabled): Boolean
  [StorageLensArn](#cfn-s3-storagelens-storagelensconfiguration-storagelensarn): String
```

## Properties<a name="aws-properties-s3-storagelens-storagelensconfiguration-properties"></a>

`AccountLevel`  <a name="cfn-s3-storagelens-storagelensconfiguration-accountlevel"></a>
This property contains the details of the account\-level metrics for Amazon S3 Storage Lens configuration\.  
*Required*: Yes  
*Type*: [AccountLevel](aws-properties-s3-storagelens-accountlevel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsOrg`  <a name="cfn-s3-storagelens-storagelensconfiguration-awsorg"></a>
This property contains the details of the AWS Organization for the S3 Storage Lens configuration\.  
*Required*: No  
*Type*: [AwsOrg](aws-properties-s3-storagelens-awsorg.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataExport`  <a name="cfn-s3-storagelens-storagelensconfiguration-dataexport"></a>
This property contains the details of this S3 Storage Lens configuration's metrics export\.  
*Required*: No  
*Type*: [DataExport](aws-properties-s3-storagelens-dataexport.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exclude`  <a name="cfn-s3-storagelens-storagelensconfiguration-exclude"></a>
This property contains the details of the bucket and or Regions excluded for Amazon S3 Storage Lens configuration\.  
*Required*: No  
*Type*: [BucketsAndRegions](aws-properties-s3-storagelens-bucketsandregions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-storagelens-storagelensconfiguration-id"></a>
This property contains the details of the ID of the S3 Storage Lens configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Include`  <a name="cfn-s3-storagelens-storagelensconfiguration-include"></a>
This property contains the details of the bucket and or Regions included for Amazon S3 Storage Lens configuration\.  
*Required*: No  
*Type*: [BucketsAndRegions](aws-properties-s3-storagelens-bucketsandregions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsEnabled`  <a name="cfn-s3-storagelens-storagelensconfiguration-isenabled"></a>
This property contains the details of whether the Amazon S3 Storage Lens configuration is enabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageLensArn`  <a name="cfn-s3-storagelens-storagelensconfiguration-storagelensarn"></a>
This property contains the details of the ARN of the S3 Storage Lens configuration\. This property is read\-only\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)