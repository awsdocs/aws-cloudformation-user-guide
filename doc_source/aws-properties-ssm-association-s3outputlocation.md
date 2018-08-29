# AWS Systems Manager Association S3OutputLocation<a name="aws-properties-ssm-association-s3outputlocation"></a>

`S3OutputLocation` is a property of the [Systems Manager Association InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md) property that specifies an Amazon S3 bucket where you want to store the results of this request\.

## Syntax<a name="w3ab2c21c14e1931b5"></a>

### JSON<a name="aws-properties-ssm-association-s3outputlocation-syntax.json"></a>

```
{
  "[OutputS3BucketName](#cfn-ssm-association-s3outputlocation-outputs3bucketname)" : String,
  "[OutputS3KeyPrefix](#cfn-ssm-association-s3outputlocation-outputs3keyprefix)" : String
}
```

### YAML<a name="aws-properties-ssm-association-s3outputlocation-syntax.yaml"></a>

```
[OutputS3BucketName](#cfn-ssm-association-s3outputlocation-outputs3bucketname): String
[OutputS3KeyPrefix](#cfn-ssm-association-s3outputlocation-outputs3keyprefix): String
```

## Properties<a name="w3ab2c21c14e1931b7"></a>

`OutputS3BucketName`  <a name="cfn-ssm-association-s3outputlocation-outputs3bucketname"></a>
The name of the Amazon S3 bucket\.  
Minimum length of 3\. Maximum length of 63\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OutputS3KeyPrefix`  <a name="cfn-ssm-association-s3outputlocation-outputs3keyprefix"></a>
The Amazon S3 bucket subfolder\.  
Maximum length of 500\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)