# AWS::GroundStation::Config S3RecordingConfig<a name="aws-properties-groundstation-config-s3recordingconfig"></a>

 Provides information about how AWS Ground Station should save downlink data to S3\. 

## Syntax<a name="aws-properties-groundstation-config-s3recordingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-s3recordingconfig-syntax.json"></a>

```
{
  "[BucketArn](#cfn-groundstation-config-s3recordingconfig-bucketarn)" : String,
  "[Prefix](#cfn-groundstation-config-s3recordingconfig-prefix)" : String,
  "[RoleArn](#cfn-groundstation-config-s3recordingconfig-rolearn)" : String
}
```

### YAML<a name="aws-properties-groundstation-config-s3recordingconfig-syntax.yaml"></a>

```
  [BucketArn](#cfn-groundstation-config-s3recordingconfig-bucketarn): String
  [Prefix](#cfn-groundstation-config-s3recordingconfig-prefix): String
  [RoleArn](#cfn-groundstation-config-s3recordingconfig-rolearn): String
```

## Properties<a name="aws-properties-groundstation-config-s3recordingconfig-properties"></a>

`BucketArn`  <a name="cfn-groundstation-config-s3recordingconfig-bucketarn"></a>
 S3 Bucket where the data is written\. The name of the S3 Bucket provided must begin with `aws-groundstation`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-groundstation-config-s3recordingconfig-prefix"></a>
 The prefix of the S3 data object\. If you choose to use any optional keys for substitution, these values will be replaced with the corresponding information from your contact details\. For example, a prefix of `{satellite_id}/{year}/{month}/{day}/` will replaced with `fake_satellite_id/2021/01/10/`   
*Optional keys for substitution*: `{satellite_id}` \| `{config-name}` \| `{config-id}` \| `{year}` \| `{month}` \| `{day}`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-groundstation-config-s3recordingconfig-rolearn"></a>
 Defines the ARN of the role assumed for putting archives to S3\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-s3recordingconfig--examples"></a>

### Create an S3RecordingConfig<a name="aws-properties-groundstation-config-s3recordingconfig--examples--Create_an_S3RecordingConfig"></a>

The following example creates a Ground Station `S3RecordingConfig`

#### JSON<a name="aws-properties-groundstation-config-s3recordingconfig--examples--Create_an_S3RecordingConfig--json"></a>

```
{
    "S3RecordingConfig": {
      "BucketArn": "arn:aws:s3:us-west-2:123456789012:bucket-name",
      "Prefix": "{satellite_id}/{config-name}_{config-id}/{year}/{month}/{day}",
      "RoleArn": "arn:aws:iam::123456789012:role/BucketRole"
    }
}
```

#### YAML<a name="aws-properties-groundstation-config-s3recordingconfig--examples--Create_an_S3RecordingConfig--yaml"></a>

```
S3RecordingConfig:
    BucketArn: arn:aws:s3:us-west-2:123456789012:bucket-name
    Prefix: {satellite_id}/{config-name}_{config-id}/{year}/{month}/{day}
    RoleArn: arn:aws:iam::123456789012:role/BucketRole
```