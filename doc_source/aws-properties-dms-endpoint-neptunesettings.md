# AWS::DMS::Endpoint NeptuneSettings<a name="aws-properties-dms-endpoint-neptunesettings"></a>

Provides information that defines an Amazon Neptune endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about the available settings, see [ Specifying endpoint settings for Amazon Neptune as a target](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Neptune.html#CHAP_Target.Neptune.EndpointSettings) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-neptunesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-neptunesettings-syntax.json"></a>

```
{
  "[ErrorRetryDuration](#cfn-dms-endpoint-neptunesettings-errorretryduration)" : Integer,
  "[IamAuthEnabled](#cfn-dms-endpoint-neptunesettings-iamauthenabled)" : Boolean,
  "[MaxFileSize](#cfn-dms-endpoint-neptunesettings-maxfilesize)" : Integer,
  "[MaxRetryCount](#cfn-dms-endpoint-neptunesettings-maxretrycount)" : Integer,
  "[S3BucketFolder](#cfn-dms-endpoint-neptunesettings-s3bucketfolder)" : String,
  "[S3BucketName](#cfn-dms-endpoint-neptunesettings-s3bucketname)" : String,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-neptunesettings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-neptunesettings-syntax.yaml"></a>

```
  [ErrorRetryDuration](#cfn-dms-endpoint-neptunesettings-errorretryduration): Integer
  [IamAuthEnabled](#cfn-dms-endpoint-neptunesettings-iamauthenabled): Boolean
  [MaxFileSize](#cfn-dms-endpoint-neptunesettings-maxfilesize): Integer
  [MaxRetryCount](#cfn-dms-endpoint-neptunesettings-maxretrycount): Integer
  [S3BucketFolder](#cfn-dms-endpoint-neptunesettings-s3bucketfolder): String
  [S3BucketName](#cfn-dms-endpoint-neptunesettings-s3bucketname): String
  [ServiceAccessRoleArn](#cfn-dms-endpoint-neptunesettings-serviceaccessrolearn): String
```

## Properties<a name="aws-properties-dms-endpoint-neptunesettings-properties"></a>

`ErrorRetryDuration`  <a name="cfn-dms-endpoint-neptunesettings-errorretryduration"></a>
The number of milliseconds for AWS DMS to wait to retry a bulk\-load of migrated graph data to the Neptune target database before raising an error\. The default is 250\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamAuthEnabled`  <a name="cfn-dms-endpoint-neptunesettings-iamauthenabled"></a>
If you want IAM authorization enabled for this endpoint, set this parameter to `true`\. Then attach the appropriate IAM policy document to your service role specified by `ServiceAccessRoleArn`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileSize`  <a name="cfn-dms-endpoint-neptunesettings-maxfilesize"></a>
The maximum size in kilobytes of migrated graph data stored in a \.csv file before AWS DMS bulk\-loads the data to the Neptune target database\. The default is 1,048,576 KB\. If the bulk load is successful, AWS DMS clears the bucket, ready to store the next batch of migrated graph data\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetryCount`  <a name="cfn-dms-endpoint-neptunesettings-maxretrycount"></a>
The number of times for AWS DMS to retry a bulk load of migrated graph data to the Neptune target database before raising an error\. The default is 5\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketFolder`  <a name="cfn-dms-endpoint-neptunesettings-s3bucketfolder"></a>
A folder path where you want AWS DMS to store migrated graph data in the S3 bucket specified by `S3BucketName`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketName`  <a name="cfn-dms-endpoint-neptunesettings-s3bucketname"></a>
The name of the Amazon S3 bucket where AWS DMS can temporarily store migrated graph data in \.csv files before bulk\-loading it to the Neptune target database\. AWS DMS maps the SQL source data to graph data before storing it in these \.csv files\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-neptunesettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) of the service role that you created for the Neptune target endpoint\. The role must allow the `iam:PassRole` action\.  
For more information, see [ Creating an IAM Service Role for Accessing Amazon Neptune as a Target](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Neptune.html#CHAP_Target.Neptune.ServiceRole) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)