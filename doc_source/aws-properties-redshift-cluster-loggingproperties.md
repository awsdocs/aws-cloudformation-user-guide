# Amazon Redshift LoggingProperties<a name="aws-properties-redshift-cluster-loggingproperties"></a>

Use the `LoggingProperties` property of the [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md) resource to configure audit log files, containing information such as queries and connection attempts, for the cluster\. 

## Syntax<a name="aws-properties-redshift-cluster-loggingproperties-syntax"></a>

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

For more information and property constraints, see [EnableLogging](http://docs.aws.amazon.com/redshift/latest/APIReference/API_EnableLogging.html) in the *Amazon Redshift API Reference*\.

`BucketName`  <a name="cfn-redshift-cluster-loggingproperties-bucketname"></a>
The name of an existing S3 bucket where the log files are to be stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`S3KeyPrefix`  <a name="cfn-redshift-cluster-loggingproperties-s3keyprefix"></a>
The prefix applied to the log file names\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)