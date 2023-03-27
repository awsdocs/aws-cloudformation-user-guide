# AWS::CloudTrail::Trail<a name="aws-resource-cloudtrail-trail"></a>

Creates a trail that specifies the settings for delivery of log data to an Amazon S3 bucket\. 

## Syntax<a name="aws-resource-cloudtrail-trail-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudtrail-trail-syntax.json"></a>

```
{
  "Type" : "AWS::CloudTrail::Trail",
  "Properties" : {
      "[CloudWatchLogsLogGroupArn](#cfn-cloudtrail-trail-cloudwatchlogsloggrouparn)" : String,
      "[CloudWatchLogsRoleArn](#cfn-cloudtrail-trail-cloudwatchlogsrolearn)" : String,
      "[EnableLogFileValidation](#cfn-cloudtrail-trail-enablelogfilevalidation)" : Boolean,
      "[EventSelectors](#cfn-cloudtrail-trail-eventselectors)" : [ EventSelector, ... ],
      "[IncludeGlobalServiceEvents](#cfn-cloudtrail-trail-includeglobalserviceevents)" : Boolean,
      "[InsightSelectors](#cfn-cloudtrail-trail-insightselectors)" : [ InsightSelector, ... ],
      "[IsLogging](#cfn-cloudtrail-trail-islogging)" : Boolean,
      "[IsMultiRegionTrail](#cfn-cloudtrail-trail-ismultiregiontrail)" : Boolean,
      "[IsOrganizationTrail](#cfn-cloudtrail-trail-isorganizationtrail)" : Boolean,
      "[KMSKeyId](#cfn-cloudtrail-trail-kmskeyid)" : String,
      "[S3BucketName](#cfn-cloudtrail-trail-s3bucketname)" : String,
      "[S3KeyPrefix](#cfn-cloudtrail-trail-s3keyprefix)" : String,
      "[SnsTopicName](#cfn-cloudtrail-trail-snstopicname)" : String,
      "[Tags](#cfn-cloudtrail-trail-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrailName](#cfn-cloudtrail-trail-trailname)" : String
    }
}
```

### YAML<a name="aws-resource-cloudtrail-trail-syntax.yaml"></a>

```
Type: AWS::CloudTrail::Trail
Properties: 
  [CloudWatchLogsLogGroupArn](#cfn-cloudtrail-trail-cloudwatchlogsloggrouparn): String
  [CloudWatchLogsRoleArn](#cfn-cloudtrail-trail-cloudwatchlogsrolearn): String
  [EnableLogFileValidation](#cfn-cloudtrail-trail-enablelogfilevalidation): Boolean
  [EventSelectors](#cfn-cloudtrail-trail-eventselectors): 
    - EventSelector
  [IncludeGlobalServiceEvents](#cfn-cloudtrail-trail-includeglobalserviceevents): Boolean
  [InsightSelectors](#cfn-cloudtrail-trail-insightselectors): 
    - InsightSelector
  [IsLogging](#cfn-cloudtrail-trail-islogging): Boolean
  [IsMultiRegionTrail](#cfn-cloudtrail-trail-ismultiregiontrail): Boolean
  [IsOrganizationTrail](#cfn-cloudtrail-trail-isorganizationtrail): Boolean
  [KMSKeyId](#cfn-cloudtrail-trail-kmskeyid): String
  [S3BucketName](#cfn-cloudtrail-trail-s3bucketname): String
  [S3KeyPrefix](#cfn-cloudtrail-trail-s3keyprefix): String
  [SnsTopicName](#cfn-cloudtrail-trail-snstopicname): String
  [Tags](#cfn-cloudtrail-trail-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrailName](#cfn-cloudtrail-trail-trailname): String
```

## Properties<a name="aws-resource-cloudtrail-trail-properties"></a>

`CloudWatchLogsLogGroupArn`  <a name="cfn-cloudtrail-trail-cloudwatchlogsloggrouparn"></a>
Specifies a log group name using an Amazon Resource Name \(ARN\), a unique identifier that represents the log group to which CloudTrail logs are delivered\. You must use a log group that exists in your account\.  
Not required unless you specify `CloudWatchLogsRoleArn`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLogsRoleArn`  <a name="cfn-cloudtrail-trail-cloudwatchlogsrolearn"></a>
Specifies the role for the CloudWatch Logs endpoint to assume to write to a user's log group\. You must use a role that exists in your account\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableLogFileValidation`  <a name="cfn-cloudtrail-trail-enablelogfilevalidation"></a>
Specifies whether log file validation is enabled\. The default is false\.  
When you disable log file integrity validation, the chain of digest files is broken after one hour\. CloudTrail does not create digest files for log files that were delivered during a period in which log file integrity validation was disabled\. For example, if you enable log file integrity validation at noon on January 1, disable it at noon on January 2, and re\-enable it at noon on January 10, digest files will not be created for the log files delivered from noon on January 2 to noon on January 10\. The same applies whenever you stop CloudTrail logging or delete a trail\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventSelectors`  <a name="cfn-cloudtrail-trail-eventselectors"></a>
Use event selectors to further specify the management and data event settings for your trail\. By default, trails created without specific event selectors will be configured to log all read and write management events, and no data events\. When an event occurs in your account, CloudTrail evaluates the event selector for all trails\. For each trail, if the event matches any event selector, the trail processes and logs the event\. If the event doesn't match any event selector, the trail doesn't log the event\.  
You can configure up to five event selectors for a trail\.  
*Required*: No  
*Type*: List of [EventSelector](aws-properties-cloudtrail-trail-eventselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeGlobalServiceEvents`  <a name="cfn-cloudtrail-trail-includeglobalserviceevents"></a>
Specifies whether the trail is publishing events from global services such as IAM to the log files\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightSelectors`  <a name="cfn-cloudtrail-trail-insightselectors"></a>
A JSON string that contains the insight types you want to log on a trail\. `ApiCallRateInsight` and `ApiErrorRateInsight` are valid Insight types\.  
The `ApiCallRateInsight` Insights type analyzes write\-only management API calls that are aggregated per minute against a baseline API call volume\.  
The `ApiErrorRateInsight` Insights type analyzes management API calls that result in error codes\. The error is shown if the API call is unsuccessful\.  
*Required*: No  
*Type*: List of [InsightSelector](aws-properties-cloudtrail-trail-insightselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsLogging`  <a name="cfn-cloudtrail-trail-islogging"></a>
Whether the CloudTrail trail is currently logging AWS API calls\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsMultiRegionTrail`  <a name="cfn-cloudtrail-trail-ismultiregiontrail"></a>
Specifies whether the trail applies only to the current region or to all regions\. The default is false\. If the trail exists only in the current region and this value is set to true, shadow trails \(replications of the trail\) will be created in the other regions\. If the trail exists in all regions and this value is set to false, the trail will remain in the region where it was created, and its shadow trails in other regions will be deleted\. As a best practice, consider using trails that log events in all regions\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsOrganizationTrail`  <a name="cfn-cloudtrail-trail-isorganizationtrail"></a>
Specifies whether the trail is applied to all accounts in an organization in AWS Organizations, or only for the current AWS account\. The default is false, and cannot be true unless the call is made on behalf of an AWS account that is the management account or delegated administrator account for an organization in AWS Organizations\. If the trail is not an organization trail and this is set to `true`, the trail will be created in all AWS accounts that belong to the organization\. If the trail is an organization trail and this is set to `false`, the trail will remain in the current AWS account but be deleted from all member accounts in the organization\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KMSKeyId`  <a name="cfn-cloudtrail-trail-kmskeyid"></a>
Specifies the AWS KMS key ID to use to encrypt the logs delivered by CloudTrail\. The value can be an alias name prefixed by "alias/", a fully specified ARN to an alias, a fully specified ARN to a key, or a globally unique identifier\.  
CloudTrail also supports AWS KMS multi\-Region keys\. For more information about multi\-Region keys, see [Using multi\-Region keys](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html) in the * AWS Key Management Service Developer Guide*\.  
Examples:  
+ alias/MyAliasName
+ arn:aws:kms:us\-east\-2:123456789012:alias/MyAliasName
+ arn:aws:kms:us\-east\-2:123456789012:key/12345678\-1234\-1234\-1234\-123456789012
+ 12345678\-1234\-1234\-1234\-123456789012
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketName`  <a name="cfn-cloudtrail-trail-s3bucketname"></a>
Specifies the name of the Amazon S3 bucket designated for publishing log files\. See [Amazon S3 Bucket Naming Requirements](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/create_trail_naming_policy.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3KeyPrefix`  <a name="cfn-cloudtrail-trail-s3keyprefix"></a>
Specifies the Amazon S3 key prefix that comes after the name of the bucket you have designated for log file delivery\. For more information, see [Finding Your CloudTrail Log Files](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-find-log-files.html)\. The maximum length is 200 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicName`  <a name="cfn-cloudtrail-trail-snstopicname"></a>
Specifies the name of the Amazon SNS topic defined for notification of log file delivery\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudtrail-trail-tags"></a>
A custom set of tags \(key\-value pairs\) for this trail\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrailName`  <a name="cfn-cloudtrail-trail-trailname"></a>
Specifies the name of the trail\. The name must meet the following requirements:  
+ Contain only ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), periods \(\.\), underscores \(\_\), or dashes \(\-\)
+ Start with a letter or number, and end with a letter or number
+ Be between 3 and 128 characters
+ Have no adjacent periods, underscores or dashes\. Names like `my-_namespace` and `my--namespace` are not valid\.
+ Not be in IP address format \(for example, 192\.168\.5\.4\)
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudtrail-trail-return-values"></a>

### Ref<a name="aws-resource-cloudtrail-trail-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudtrail-trail-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudtrail-trail-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the CloudTrail trail, such as `arn:aws:cloudtrail:us-east-2:123456789012:trail/myCloudTrail`\.

`SnsTopicArn`  <a name="SnsTopicArn-fn::getatt"></a>
 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the Amazon SNS topic that's associated with the CloudTrail trail, such as `arn:aws:sns:us-east-2:123456789012:mySNSTopic`\.

## Examples<a name="aws-resource-cloudtrail-trail--examples"></a>



### Example<a name="aws-resource-cloudtrail-trail--examples--Example"></a>

The following example creates a trail that logs events in all regions, an Amazon S3 bucket where logs are published, and an Amazon SNS topic where notifications are sent\. The bucket and topic policies allow CloudTrail \(from the specified regions\) to publish logs to the S3 bucket and to send notifications to an email that you specify\. For information about CloudTrail bucket policies, see [Amazon S3 Bucket Policy](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/create_trail_bucket_policy.html) in the *AWS CloudTrail User Guide*\.

#### JSON<a name="aws-resource-cloudtrail-trail--examples--Example--json"></a>

```
{
    "Parameters": {
        "TrailName": {
            "Type": "String"
        },
        "BucketName": {
            "Type": "String"
        }
    },
    "Conditions": {
        "IsOrganizationsSupported": {
            "Fn::Equals": [
                {
                    "Ref": "AWS::Partition"
                },
                "aws"
            ]
        }
    },
    "Resources": {
        "Trail": {
            "Type": "AWS::CloudTrail::Trail",
            "Properties": {
                "S3BucketName": {
                    "Ref": "BucketName"
                },
                "S3KeyPrefix": "Uluru",
                "IsLogging": true,
                "TrailName": {
                    "Ref": "TrailName"
                },
                "EnableLogFileValidation": true,
                "IncludeGlobalServiceEvents": true,
                "IsMultiRegionTrail": true,
                "CloudWatchLogsLogGroupArn": {
                    "Fn::ImportValue": "TrailLogGroupTestArn"
                },
                "CloudWatchLogsRoleArn": {
                    "Fn::ImportValue": "TrailLogGroupRoleTestArn"
                },
                "KMSKeyId": {
                    "Fn::ImportValue": "TrailKeyTest"
                },
                "Tags": [
                    {
                        "Key": "TagKeyIntTest",
                        "Value": "TagValueIntTest"
                    },
                    {
                        "Key": "TagKeyIntTest2",
                        "Value": "TagValueIntTest2"
                    }
                ],
                "SnsTopicName": {
                    "Fn::ImportValue": "TrailTopicTest"
                },
                "EventSelectors": [
                    {
                        "DataResources": [
                            {
                                "Type": "AWS::S3::Object",
                                "Values": [
                                    {
                                        "Fn::Sub": "arn:${AWS::Partition}:s3"
                                    }
                                ]
                            }
                        ],
                        "IncludeManagementEvents": true,
                        "ReadWriteType": "All"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "ARN": {
            "Description": "The trail ARN",
            "Value": {
                "Fn::GetAtt": [
                    "Trail",
                    "Arn"
                ]
            }
        },
        "TopicArn": {
            "Description": "The SnS Topic ARN",
            "Value": {
                "Fn::GetAtt": [
                    "Trail",
                    "SnsTopicArn"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudtrail-trail--examples--Example--yaml"></a>

```
Parameters:
  TrailName:
    Type: String
  BucketName:
    Type: String
Conditions:
  IsOrganizationsSupported:
    Fn::Equals:
      - { Ref: "AWS::Partition" }
      - "aws"
Resources:
  Trail:
    Type: AWS::CloudTrail::Trail
    Properties:
      S3BucketName: !Ref BucketName
      S3KeyPrefix: "Uluru"
      IsLogging: true
      TrailName: !Ref TrailName
      EnableLogFileValidation: true
      IncludeGlobalServiceEvents: true
      IsMultiRegionTrail: true
      CloudWatchLogsLogGroupArn:
        Fn::ImportValue: "TrailLogGroupTestArn"
      CloudWatchLogsRoleArn:
        Fn::ImportValue: "TrailLogGroupRoleTestArn"
      KMSKeyId:
        Fn::ImportValue: TrailKeyTest
      Tags:
        - Key: "TagKeyIntTest"
          Value: "TagValueIntTest"
        - Key: "TagKeyIntTest2"
          Value: "TagValueIntTest2"
      SnsTopicName:
        Fn::ImportValue: TrailTopicTest
      EventSelectors:
        - DataResources:
            - Type: AWS::S3::Object
              Values:
                - !Sub "arn:${AWS::Partition}:s3"
          IncludeManagementEvents: true
          ReadWriteType: All
Outputs:
  ARN:
    Description: The trail ARN
    Value:
      'Fn::GetAtt':
        - Trail
        - Arn
  TopicArn:
    Description: The SnS Topic ARN
    Value:
      'Fn::GetAtt':
        - Trail
        - SnsTopicArn
```