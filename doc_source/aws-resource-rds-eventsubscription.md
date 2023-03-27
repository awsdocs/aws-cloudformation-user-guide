# AWS::RDS::EventSubscription<a name="aws-resource-rds-eventsubscription"></a>

The `AWS::RDS::EventSubscription` resource allows you to receive notifications for Amazon Relational Database Service events through the Amazon Simple Notification Service \(Amazon SNS\)\. For more information, see [Using Amazon RDS Event Notification](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.html) in the *Amazon RDS User Guide*\. 

## Syntax<a name="aws-resource-rds-eventsubscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-eventsubscription-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::EventSubscription",
  "Properties" : {
      "[Enabled](#cfn-rds-eventsubscription-enabled)" : Boolean,
      "[EventCategories](#cfn-rds-eventsubscription-eventcategories)" : [ String, ... ],
      "[SnsTopicArn](#cfn-rds-eventsubscription-snstopicarn)" : String,
      "[SourceIds](#cfn-rds-eventsubscription-sourceids)" : [ String, ... ],
      "[SourceType](#cfn-rds-eventsubscription-sourcetype)" : String,
      "[SubscriptionName](#cfn-rds-eventsubscription-subscriptionname)" : String,
      "[Tags](#cfn-rds-eventsubscription-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-eventsubscription-syntax.yaml"></a>

```
Type: AWS::RDS::EventSubscription
Properties: 
  [Enabled](#cfn-rds-eventsubscription-enabled): Boolean
  [EventCategories](#cfn-rds-eventsubscription-eventcategories): 
    - String
  [SnsTopicArn](#cfn-rds-eventsubscription-snstopicarn): String
  [SourceIds](#cfn-rds-eventsubscription-sourceids): 
    - String
  [SourceType](#cfn-rds-eventsubscription-sourcetype): String
  [SubscriptionName](#cfn-rds-eventsubscription-subscriptionname): String
  [Tags](#cfn-rds-eventsubscription-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-eventsubscription-properties"></a>

`Enabled`  <a name="cfn-rds-eventsubscription-enabled"></a>
A value that indicates whether to activate the subscription\. If the event notification subscription isn't activated, the subscription is created but not active\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventCategories`  <a name="cfn-rds-eventsubscription-eventcategories"></a>
A list of event categories for a particular source type \(`SourceType`\) that you want to subscribe to\. You can see a list of the categories for a given source type in the "Amazon RDS event categories and event messages" section of the [https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.Messages.html](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.Messages.html) or the [https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_Events.Messages.html](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_Events.Messages.html)\. You can also see this list by using the `DescribeEventCategories` operation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicArn`  <a name="cfn-rds-eventsubscription-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the SNS topic created for event notification\. The ARN is created by Amazon SNS when you create a topic and subscribe to it\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceIds`  <a name="cfn-rds-eventsubscription-sourceids"></a>
The list of identifiers of the event sources for which events are returned\. If not specified, then all sources are included in the response\. An identifier must begin with a letter and must contain only ASCII letters, digits, and hyphens\. It can't end with a hyphen or contain two consecutive hyphens\.  
Constraints:  
+ If a `SourceIds` value is supplied, `SourceType` must also be provided\.
+ If the source type is a DB instance, a `DBInstanceIdentifier` value must be supplied\.
+ If the source type is a DB cluster, a `DBClusterIdentifier` value must be supplied\.
+ If the source type is a DB parameter group, a `DBParameterGroupName` value must be supplied\.
+ If the source type is a DB security group, a `DBSecurityGroupName` value must be supplied\.
+ If the source type is a DB snapshot, a `DBSnapshotIdentifier` value must be supplied\.
+ If the source type is a DB cluster snapshot, a `DBClusterSnapshotIdentifier` value must be supplied\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceType`  <a name="cfn-rds-eventsubscription-sourcetype"></a>
The type of source that is generating the events\. For example, if you want to be notified of events generated by a DB instance, set this parameter to `db-instance`\. If this value isn't specified, all events are returned\.  
Valid values: `db-instance` \| `db-cluster` \| `db-parameter-group` \| `db-security-group` \| `db-snapshot` \| `db-cluster-snapshot`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubscriptionName`  <a name="cfn-rds-eventsubscription-subscriptionname"></a>
The name of the subscription\.  
Constraints: The name must be less than 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rds-eventsubscription-tags"></a>
An optional array of key\-value pairs to apply to this subscription\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-eventsubscription-return-values"></a>

### Ref<a name="aws-resource-rds-eventsubscription-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the RDS event subscription\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-eventsubscription--examples"></a>



### <a name="aws-resource-rds-eventsubscription--examples--"></a>

The following example creates an event subscription for an existing database instance `db-instance-1` and a database with the logical ID `myDBInstance`, which is declared elsewhere in the same template\. 

#### JSON<a name="aws-resource-rds-eventsubscription--examples----json"></a>

```
{
    "myEventSubscription": {
        "Type": "AWS::RDS::EventSubscription",
        "Properties": {
            "EventCategories": [
                "configuration change",
                "failure",
                "deletion"
            ],
            "SnsTopicArn": "arn:aws:sns:us-west-2:123456789012:example-topic",
            "SourceIds": [
                "db-instance-1",
                {
                    "Ref": "myDBInstance"
                }
            ],
            "SourceType": "db-instance",
            "Enabled": false
        }
    }
}
```

#### YAML<a name="aws-resource-rds-eventsubscription--examples----yaml"></a>

```
--- 
myEventSubscription:
  Type: 'AWS::RDS::EventSubscription'
  Properties:
    EventCategories:
      - configuration change
      - failure
      - deletion
    SnsTopicArn: 'arn:aws:sns:us-west-2:123456789012:example-topic'
    SourceIds:
      - db-instance-1
      - !Ref myDBInstance
    SourceType: db-instance
    Enabled: false
```