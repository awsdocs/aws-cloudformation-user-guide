# Amazon Simple Storage Service Bucket LambdaConfiguration<a name="aws-properties-s3-bucket-notificationconfig-lambdaconfig"></a>

`LambdaConfigurations` is a property of the [Amazon S3 Bucket NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md) property that describes the AWS Lambda \(Lambda\) functions to invoke and the events for which to invoke them\.

## Syntax<a name="w4ab1c21c14e1829b5"></a>

### JSON<a name="aws-properties-s3-bucket-notificationconfig-lambdaconfig-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-notificationconfig-lambdaconfig-event)" : String,
  "[Filter](#cfn-s3-bucket-notificationconfig-lambdaconfig-filter)" : Filter,
  "[Function](#cfn-s3-bucket-notificationconfig-lambdaconfig-function)" : String 
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-lambdaconfig-syntax.yaml"></a>

```
[Event](#cfn-s3-bucket-notificationconfig-lambdaconfig-event): String
[Filter](#cfn-s3-bucket-notificationconfig-lambdaconfig-filter):
  Filter
[Function](#cfn-s3-bucket-notificationconfig-lambdaconfig-function): String
```

## Properties<a name="w4ab1c21c14e1829b7"></a>

`Event`  <a name="cfn-s3-bucket-notificationconfig-lambdaconfig-event"></a>
The S3 bucket event for which to invoke the Lambda function\. For more information, see [Supported Event Types](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String

`Filter`  <a name="cfn-s3-bucket-notificationconfig-lambdaconfig-filter"></a>
The filtering rules that determine which objects invoke the Lambda function\. For example, you can create a filter so that only image files with a `.jpg` extension invoke the function when they are added to the S3 bucket\.  
*Required*: No  
*Type*: [Amazon S3 Bucket NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md)

`Function`  <a name="cfn-s3-bucket-notificationconfig-lambdaconfig-function"></a>
The Amazon Resource Name \(ARN\) of the Lambda function that Amazon S3 invokes when the specified event type occurs\.  
*Required*: Yes  
*Type*: String

## Example<a name="w4ab1c21c14e1829b9"></a>

The following example creates a `NotificationConfiguration` for Lambda using an S3 bucket named `EncryptionServiceBucket`\.

**Note**  
The `BucketName` is unique and the `Value` contains a file extension without a period \(`.`\)\.

### JSON<a name="example.json"></a>

```
"EncryptionServiceBucket" : {
  "Type" : "AWS::S3::Bucket",
  "Properties" : {
    "BucketName" : { "Fn::Sub" : "${User}-encryption-service" },
    "NotificationConfiguration" : {
      "LambdaConfigurations" : [{
        "Function" : { "Ref" : "LambdaDeploymentArn" },
        "Event" : "s3:ObjectCreated:*",
        "Filter" : {
          "S3Key" : {
            "Rules" : [{
              "Name" : "suffix",
              "Value" : "zip"
            }]
          }
        }
      }]
    }
  }
}
```

### YAML<a name="example.yaml"></a>

```
EncryptionServiceBucket:
  Type: AWS::S3::Bucket
  Properties:
    BucketName: !Sub ${User}-encryption-service
    NotificationConfiguration:
      LambdaConfigurations:
        -
          Function: !Ref LambdaDeploymentArn
          Event: "s3:ObjectCreated:*"
          Filter:
            S3Key:
              Rules:
                -
                  Name: suffix
                  Value: zip
```