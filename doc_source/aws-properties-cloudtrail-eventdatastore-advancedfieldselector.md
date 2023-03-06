# AWS::CloudTrail::EventDataStore AdvancedFieldSelector<a name="aws-properties-cloudtrail-eventdatastore-advancedfieldselector"></a>

A single selector statement in an advanced event selector\.

## Syntax<a name="aws-properties-cloudtrail-eventdatastore-advancedfieldselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-eventdatastore-advancedfieldselector-syntax.json"></a>

```
{
  "[EndsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-endswith)" : [ String, ... ],
  "[Equals](#cfn-cloudtrail-eventdatastore-advancedfieldselector-equals)" : [ String, ... ],
  "[Field](#cfn-cloudtrail-eventdatastore-advancedfieldselector-field)" : String,
  "[NotEndsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notendswith)" : [ String, ... ],
  "[NotEquals](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notequals)" : [ String, ... ],
  "[NotStartsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notstartswith)" : [ String, ... ],
  "[StartsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-startswith)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudtrail-eventdatastore-advancedfieldselector-syntax.yaml"></a>

```
  [EndsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-endswith): 
    - String
  [Equals](#cfn-cloudtrail-eventdatastore-advancedfieldselector-equals): 
    - String
  [Field](#cfn-cloudtrail-eventdatastore-advancedfieldselector-field): String
  [NotEndsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notendswith): 
    - String
  [NotEquals](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notequals): 
    - String
  [NotStartsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-notstartswith): 
    - String
  [StartsWith](#cfn-cloudtrail-eventdatastore-advancedfieldselector-startswith): 
    - String
```

## Properties<a name="aws-properties-cloudtrail-eventdatastore-advancedfieldselector-properties"></a>

`EndsWith`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-endswith"></a>
An operator that includes events that match the last few characters of the event record field specified as the value of `Field`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Equals`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-equals"></a>
 An operator that includes events that match the exact value of the event record field specified as the value of `Field`\. This is the only valid operator that you can use with the `readOnly`, `eventCategory`, and `resources.type` fields\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Field`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-field"></a>
 A field in a CloudTrail event record on which to filter events to be logged\. For event data stores for AWS Config configuration items, Audit Manager evidence, or non\-AWS events, the field is used only for selecting events as filtering is not supported\.   
 For CloudTrail event records, supported fields include `readOnly`, `eventCategory`, `eventSource` \(for management events\), `eventName`, `resources.type`, and `resources.ARN`\.   
 For event data stores for AWS Config configuration items, Audit Manager evidence, or non\-AWS events, the only supported field is `eventCategory`\.   
+  ** `readOnly` ** \- Optional\. Can be set to `Equals` a value of `true` or `false`\. If you do not add this field, CloudTrail logs both `read` and `write` events\. A value of `true` logs only `read` events\. A value of `false` logs only `write` events\.
+  ** `eventSource` ** \- For filtering management events only\. This can be set only to `NotEquals` `kms.amazonaws.com`\.
+  ** `eventName` ** \- Can use any operator\. You can use it to ﬁlter in or ﬁlter out any data event logged to CloudTrail, such as `PutBucket` or `GetSnapshotBlock`\. You can have multiple values for this ﬁeld, separated by commas\.
+  ** `eventCategory` ** \- This is required and must be set to `Equals`\. 
  +  For CloudTrail event records, the value must be `Management` or `Data`\. 
  +  For AWS Config configuration items, the value must be `ConfigurationItem`\. 
  +  For Audit Manager evidence, the value must be `Evidence`\. 
  +  For non\-AWS events, the value must be `ActivityAuditLog`\. 
+  ** `resources.type` ** \- This ﬁeld is required for CloudTrail data events\. `resources.type` can only use the `Equals` operator, and the value can be one of the following:
  +  `AWS::DynamoDB::Table` 
  +  `AWS::Lambda::Function` 
  +  `AWS::S3::Object` 
  +  `AWS::CloudTrail::Channel` 
  +  `AWS::Cognito::IdentityPool` 
  +  `AWS::DynamoDB::Stream` 
  +  `AWS::EC2::InstanceConnectEndpoint` 
  +  `AWS::EC2::Snapshot` 
  +  `AWS::FinSpace::Environment` 
  +  `AWS::Glue::Table` 
  +  `AWS::KendraRanking::ExecutionPlan` 
  +  `AWS::ManagedBlockchain::Node` 
  +  `AWS::SageMaker::ExperimentTrialComponent` 
  +  `AWS::SageMaker::FeatureGroup` 
  +  `AWS::S3::AccessPoint` 
  +  `AWS::S3ObjectLambda::AccessPoint` 
  +  `AWS::S3Outposts::Object` 

   You can have only one `resources.type` ﬁeld per selector\. To log data events on more than one resource type, add another selector\.
+  ** `resources.ARN` ** \- You can use any operator with `resources.ARN`, but if you use `Equals` or `NotEquals`, the value must exactly match the ARN of a valid resource of the type you've speciﬁed in the template as the value of resources\.type\. For example, if resources\.type equals `AWS::S3::Object`, the ARN must be in one of the following formats\. To log all data events for all objects in a specific S3 bucket, use the `StartsWith` operator, and include only the bucket ARN as the matching value\.

  The trailing slash is intentional; do not exclude it\. Replace the text between less than and greater than symbols \(<>\) with resource\-specific information\. 
  +  `arn:<partition>:s3:::<bucket_name>/` 
  +  `arn:<partition>:s3:::<bucket_name>/<object_path>/` 

  When resources\.type equals `AWS::DynamoDB::Table`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:dynamodb:<region>:<account_ID>:table/<table_name>` 

  When resources\.type equals `AWS::Lambda::Function`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:lambda:<region>:<account_ID>:function:<function_name>` 

  When resources\.type equals `AWS::CloudTrail::Channel`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:cloudtrail:<region>:<account_ID>:channel/<channel_UUID>` 

  When resources\.type equals `AWS::Cognito::IdentityPool`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:cognito-identity:<region>:<account_ID>:identitypool/<identity_pool_ID>` 

  When `resources.type` equals `AWS::DynamoDB::Stream`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:dynamodb:<region>:<account_ID>:table/<table_name>/stream/<date_time>` 

  When `resources.type` equals `AWS::EC2::InstanceConnectEndpoint`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:ec2:<region>::instance-connect-endpoint/<instance_connect_endpoint_ID>` 

  When `resources.type` equals `AWS::EC2::Snapshot`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:ec2:<region>::snapshot/<snapshot_ID>` 

  When `resources.type` equals `AWS::FinSpace::Environment`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:finspace:<region>:<account_ID>:environment/<environment_ID>` 

  When `resources.type` equals `AWS::Glue::Table`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:glue:<region>:<account_ID>:table/<database_name>/<table_name>` 

  When `resources.type` equals `AWS::KendraRanking::ExecutionPlan`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:kendra-ranking:<region>:<account_ID>:table/<rescore-execution-plan>/<rescore_execution_plan_ID>` 

  When `resources.type` equals `AWS::ManagedBlockchain::Node`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:managedblockchain:<region>:<account_ID>:nodes/<node_ID>` 

  When `resources.type` equals `AWS::SageMaker::ExperimentTrialComponent`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:sagemaker:<region>:<account_ID>:experiment-trial-component/<experiment_trial_component_name>` 

  When `resources.type` equals `AWS::SageMaker::FeatureGroup`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:sagemaker:<region>:<account_ID>:feature-group/<feature_group_name>` 

  When `resources.type` equals `AWS::S3::AccessPoint`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in one of the following formats\. To log events on all objects in an S3 access point, we recommend that you use only the access point ARN, don’t include the object path, and use the `StartsWith` or `NotStartsWith` operators\.
  +  `arn:<partition>:s3:<region>:<account_ID>:accesspoint/<access_point_name>` 
  +  `arn:<partition>:s3:<region>:<account_ID>:accesspoint/<access_point_name>/object/<object_path>` 

  When `resources.type` equals `AWS::S3ObjectLambda::AccessPoint`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:s3-object-lambda:<region>:<account_ID>:accesspoint/<access_point_name>` 

  When `resources.type` equals `AWS::S3Outposts::Object`, and the operator is set to `Equals` or `NotEquals`, the ARN must be in the following format:
  +  `arn:<partition>:s3-outposts:<region>:<account_ID>:<object_path>` 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `[\w|\d|\.|_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotEndsWith`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-notendswith"></a>
 An operator that excludes events that match the last few characters of the event record field specified as the value of `Field`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotEquals`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-notequals"></a>
 An operator that excludes events that match the exact value of the event record field specified as the value of `Field`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotStartsWith`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-notstartswith"></a>
 An operator that excludes events that match the first few characters of the event record field specified as the value of `Field`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartsWith`  <a name="cfn-cloudtrail-eventdatastore-advancedfieldselector-startswith"></a>
An operator that includes events that match the first few characters of the event record field specified as the value of `Field`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)