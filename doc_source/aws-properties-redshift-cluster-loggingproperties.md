# AWS::Redshift::Cluster LoggingProperties<a name="aws-properties-redshift-cluster-loggingproperties"></a>

Specifies logging information, such as queries and connection attempts, for the specified Amazon Redshift cluster\.

## Syntax<a name="aws-properties-redshift-cluster-loggingproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshift-cluster-loggingproperties-syntax.json"></a>

```
{
  "[BucketName](#cfn-redshift-cluster-loggingproperties-bucketname)" : String,
  "[S3KeyPrefix](#cfn-redshift-cluster-loggingproperties-s3keyprefix)" : String
}
```

### YAML<a name="aws-properties-redshift-cluster-loggingproperties-syntax.yaml"></a>

```
  [BucketName](#cfn-redshift-cluster-loggingproperties-bucketname): String
  [S3KeyPrefix](#cfn-redshift-cluster-loggingproperties-s3keyprefix): String
```

## Properties<a name="aws-properties-redshift-cluster-loggingproperties-properties"></a>

`BucketName`  <a name="cfn-redshift-cluster-loggingproperties-bucketname"></a>
The name of an existing S3 bucket where the log files are to be stored\.  
Constraints:  
+ Must be in the same region as the cluster
+ The cluster must have read bucket and put object permissions
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3KeyPrefix`  <a name="cfn-redshift-cluster-loggingproperties-s3keyprefix"></a>
The prefix applied to the log file names\.  
Constraints:  
+ Cannot exceed 512 characters
+ Cannot contain spaces\( \), double quotes \("\), single quotes \('\), a backslash \(\\\), or control characters\. The hexadecimal codes for invalid characters are: 
  + x00 to x20
  + x22
  + x27
  + x5c
  + x7f or larger
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)