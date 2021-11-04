# AWS::IoTAnalytics::Datastore CustomerManagedS3Storage<a name="aws-properties-iotanalytics-datastore-customermanageds3storage"></a>

Amazon S3\-customer\-managed; When you choose customer\-managed storage, the `retentionPeriod` parameter is ignored\. You can't change the choice of Amazon S3 storage after your data store is created\.

## Syntax<a name="aws-properties-iotanalytics-datastore-customermanageds3storage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-customermanageds3storage-syntax.json"></a>

```
{
  "[Bucket](#cfn-iotanalytics-datastore-customermanageds3storage-bucket)" : String,
  "[KeyPrefix](#cfn-iotanalytics-datastore-customermanageds3storage-keyprefix)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-customermanageds3storage-syntax.yaml"></a>

```
  [Bucket](#cfn-iotanalytics-datastore-customermanageds3storage-bucket): String
  [KeyPrefix](#cfn-iotanalytics-datastore-customermanageds3storage-keyprefix): String
```

## Properties<a name="aws-properties-iotanalytics-datastore-customermanageds3storage-properties"></a>

`Bucket`  <a name="cfn-iotanalytics-datastore-customermanageds3storage-bucket"></a>
The name of the Amazon S3 bucket where your data is stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefix`  <a name="cfn-iotanalytics-datastore-customermanageds3storage-keyprefix"></a>
\(Optional\) The prefix used to create the keys of the data store data objects\. Each object in an Amazon S3 bucket has a key that is its unique identifier in the bucket\. Each object in a bucket has exactly one key\. The prefix must end with a forward slash \(/\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)