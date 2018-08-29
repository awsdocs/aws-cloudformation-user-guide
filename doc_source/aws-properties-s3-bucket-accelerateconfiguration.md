# Amazon S3 Bucket AccelerateConfiguration<a name="aws-properties-s3-bucket-accelerateconfiguration"></a>

<a name="aws-properties-s3-bucket-accelerateconfiguration-description"></a>The `AccelerateConfiguration` property type configures the transfer acceleration state for an Amazon S3 bucket\. For more information, see [Amazon S3 Transfer Acceleration](http://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html) in the *Amazon Simple Storage Service Developer Guide*\.

<a name="aws-properties-s3-bucket-accelerateconfiguration-inheritance"></a> `AccelerateConfiguration` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource\.

## Syntax<a name="aws-properties-s3-bucket-accelerateconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-accelerateconfiguration-syntax.json"></a>

```
{
  "[AccelerationStatus](#cfn-s3-bucket-accelerateconfiguration-accelerationstatus)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-accelerateconfiguration-syntax.yaml"></a>

```
[AccelerationStatus](#cfn-s3-bucket-accelerateconfiguration-accelerationstatus): String
```

## Properties<a name="aws-properties-s3-bucket-accelerateconfiguration-properties"></a>

`AccelerationStatus`  <a name="cfn-s3-bucket-accelerateconfiguration-accelerationstatus"></a>
Sets the transfer acceleration state of the bucket\.  
 *Required*: Yes  
 *Type*: String  
*Valid values*: `Enabled`, `Suspended`  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Example<a name="aws-properties-s3-bucket-accelerateconfiguration-examples"></a>

### <a name="aws-properties-s3-bucket-accelerateconfiguration-example1"></a>

The following example sets the transfer acceleration state of a bucket based on the `AccelerateStatus` parameter\.

#### JSON<a name="aws-properties-s3-bucket-accelerateconfiguration-example1.json"></a>

```
{
	"AWSTemplateFormatVersion":"2010-09-09",
	"Parameters" : {
		"AccelerateStatus" : {
			"Type" : "String"
		}
	},
	"Resources":{
		"MyBucket":{
			"Type":"AWS::S3::Bucket",
			"Properties" : {
				"AccelerateConfiguration" : {
					"AccelerationStatus" : {"Ref" : "AccelerateStatus"}
				}
			}
		}
	}
}
```

#### YAML<a name="aws-properties-s3-bucket-accelerateconfiguration-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AccelerateStatus:
    Type: String
Resources:
  MyBucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccelerateConfiguration:
        AccelerationStatus: !Ref AccelerateStatus
```