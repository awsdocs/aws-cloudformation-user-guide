# AWS::Logs::LogGroup<a name="aws-resource-logs-loggroup"></a>

The `AWS::Logs::LogGroup` resource specifies a log group\. A log group defines common properties for log streams, such as their retention and access control rules\. Each log stream must belong to one log group\.

You can create up to 1,000,000 log groups per Region per account\. You must use the following guidelines when naming a log group:
+ Log group names must be unique within a Region for an AWS account\.
+ Log group names can be between 1 and 512 characters long\.
+ Log group names consist of the following characters: a\-z, A\-Z, 0\-9, '\_' \(underscore\), '\-' \(hyphen\), '/' \(forward slash\), and '\.' \(period\)\.

## Syntax<a name="aws-resource-logs-loggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-loggroup-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::LogGroup",
  "Properties" : {
      "[DataProtectionPolicy](#cfn-logs-loggroup-dataprotectionpolicy)" : Json,
      "[KmsKeyId](#cfn-logs-loggroup-kmskeyid)" : String,
      "[LogGroupName](#cfn-logs-loggroup-loggroupname)" : String,
      "[RetentionInDays](#cfn-logs-loggroup-retentionindays)" : Integer,
      "[Tags](#cfn-logs-loggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-logs-loggroup-syntax.yaml"></a>

```
Type: AWS::Logs::LogGroup
Properties: 
  [DataProtectionPolicy](#cfn-logs-loggroup-dataprotectionpolicy): Json
  [KmsKeyId](#cfn-logs-loggroup-kmskeyid): String
  [LogGroupName](#cfn-logs-loggroup-loggroupname): String
  [RetentionInDays](#cfn-logs-loggroup-retentionindays): Integer
  [Tags](#cfn-logs-loggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-logs-loggroup-properties"></a>

`DataProtectionPolicy`  <a name="cfn-logs-loggroup-dataprotectionpolicy"></a>
Creates a data protection policy and assigns it to the log group\. A data protection policy can help safeguard sensitive data that's ingested by the log group by auditing and masking the sensitive log data\. When a user who does not have permission to view masked data views a log event that includes masked data, the sensitive data is replaced by asterisks\.  
For more information, including a list of types of data that can be audited and masked, see [Protect sensitive log data with masking](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/mask-sensitive-log-data.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-logs-loggroup-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS key to use when encrypting log data\.  
To associate an AWS KMS key with the log group, specify the ARN of that KMS key here\. If you do so, ingested data is encrypted using this key\. This association is stored as long as the data encrypted with the KMS key is still within CloudWatch Logs\. This enables CloudWatch Logs to decrypt this data whenever it is requested\.  
If you attempt to associate a KMS key with the log group but the KMS key doesn't exist or is deactivated, you will receive an `InvalidParameterException` error\.  
Log group data is always encrypted in CloudWatch Logs\. If you omit this key, the encryption does not use AWS KMS\. For more information, see [ Encrypt log data in CloudWatch Logs using AWS Key Management Service](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/encrypt-log-data-kms.html)   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-logs-loggroup-loggroupname"></a>
The name of the log group\. If you don't specify a name, AWS CloudFormation generates a unique ID for the log group\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RetentionInDays`  <a name="cfn-logs-loggroup-retentionindays"></a>
The number of days to retain the log events in the specified log group\. Possible values are: 1, 3, 5, 7, 14, 30, 60, 90, 120, 150, 180, 365, 400, 545, 731, 1827, 2192, 2557, 2922, 3288, and 3653\.  
To set a log group so that its log events do not expire, use [DeleteRetentionPolicy](https://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_DeleteRetentionPolicy.html)\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-logs-loggroup-tags"></a>
An array of key\-value pairs to apply to the log group\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-logs-loggroup-return-values"></a>

### Ref<a name="aws-resource-logs-loggroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-logs-loggroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-logs-loggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the log group, such as `arn:aws:logs:us-west-1:123456789012:log-group:/mystack-testgroup-12ABC1AB12A1:*`

## Examples<a name="aws-resource-logs-loggroup--examples"></a>



### Create a log group<a name="aws-resource-logs-loggroup--examples--Create_a_log_group"></a>

The following example creates a log group that retains events for 7 days\.

#### JSON<a name="aws-resource-logs-loggroup--examples--Create_a_log_group--json"></a>

```
"myLogGroup": {
    "Type": "AWS::Logs::LogGroup",
    "Properties": {
        "RetentionInDays": 7
    }
}
```

#### YAML<a name="aws-resource-logs-loggroup--examples--Create_a_log_group--yaml"></a>

```
myLogGroup: 
  Type: AWS::Logs::LogGroup
  Properties: 
    RetentionInDays: 7
```

### Create a log group with a data protection policy<a name="aws-resource-logs-loggroup--examples--Create_a_log_group_with_a_data_protection_policy"></a>

The following example creates a log group that uses a data protection policy to mask email addresses, and send audit findings to CloudWatch Logs, Kinesis Data Firehose, and Amazon S3\.

#### JSON<a name="aws-resource-logs-loggroup--examples--Create_a_log_group_with_a_data_protection_policy--json"></a>

```
"TestLogGroupDescription": {
  "Type": "AWS::Logs::LogGroup",
  "Properties": {
      "LogGroupName": "my-log-group",
      "DataProtectionPolicy": {
          "Name": "data-protection-policy",
          "Description": "test description",
          "Version": "2021-06-01",
          "Statement": [{
                  "Sid": "audit-policy test",
                  "DataIdentifier": [
                      "arn:aws:dataprotection::aws:data-identifier/EmailAddress",
                      "arn:aws:dataprotection::aws:data-identifier/DriversLicense-US"
                  ],
                  "Operation": {
                      "Audit": {
                          "FindingsDestination": {
                              "CloudWatchLogs": {
                                  "LogGroup": "EXISTING_LOG_GROUP_IN_YOUR_ACCOUNT"
                              },
                              "Firehose": {
                                  "DeliveryStream": "EXISTING_STREAM_IN_YOUR_ACCOUNT"
                              },
                              "S3": {
                                  "Bucket": "EXISTING_BUCKET"
                              }
                          }
                      }
                  }
              },
              {
                  "Sid": "redact-policy",
                  "DataIdentifier": [
                      "arn:aws:dataprotection::aws:data-identifier/EmailAddress",
                      "arn:aws:dataprotection::aws:data-identifier/DriversLicense-US"
                  ],
                  "Operation": {
                      "Deidentify": {
                          "MaskConfig": {}
                      }
                  }
              }
          ]
      }
  }
}
```

#### YAML<a name="aws-resource-logs-loggroup--examples--Create_a_log_group_with_a_data_protection_policy--yaml"></a>

```
TestLogGroupDescription:
  Type: AWS::Logs::LogGroup
  Properties:
    LogGroupName: my-log-group
    DataProtectionPolicy:
      Name: data-protection-policy
      Description: test description
      Version: '2021-06-01'
      Statement:
      - Sid: audit-policy test
        DataIdentifier:
        - arn:aws:dataprotection::aws:data-identifier/EmailAddress
        - arn:aws:dataprotection::aws:data-identifier/DriversLicense-US
        Operation:
          Audit:
            FindingsDestination:
              CloudWatchLogs:
                LogGroup: EXISTING_LOG_GROUP_IN_YOUR_ACCOUNT
              Firehose:
                DeliveryStream: EXISTING_STREAM_IN_YOUR_ACCOUNT
              S3:
                Bucket: EXISTING_BUCKET
      - Sid: redact-policy
        DataIdentifier:
        - arn:aws:dataprotection::aws:data-identifier/EmailAddress
        - arn:aws:dataprotection::aws:data-identifier/DriversLicense-US
        Operation:
          Deidentify:
            MaskConfig: {}
```