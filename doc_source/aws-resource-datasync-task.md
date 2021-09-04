# AWS::DataSync::Task<a name="aws-resource-datasync-task"></a>

The `AWS::DataSync::Task` resource specifies a task\. A task is a set of two locations \(source and destination\) and a set of Options that you use to control the behavior of a task\. If you don't specify Options when you create a task, AWS DataSync populates them with service defaults\.

## Syntax<a name="aws-resource-datasync-task-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-task-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::Task",
  "Properties" : {
      "[CloudWatchLogGroupArn](#cfn-datasync-task-cloudwatchloggrouparn)" : String,
      "[DestinationLocationArn](#cfn-datasync-task-destinationlocationarn)" : String,
      "[Excludes](#cfn-datasync-task-excludes)" : [ FilterRule, ... ],
      "[Includes](#cfn-datasync-task-includes)" : [ FilterRule, ... ],
      "[Name](#cfn-datasync-task-name)" : String,
      "[Options](#cfn-datasync-task-options)" : Options,
      "[Schedule](#cfn-datasync-task-schedule)" : TaskSchedule,
      "[SourceLocationArn](#cfn-datasync-task-sourcelocationarn)" : String,
      "[Tags](#cfn-datasync-task-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-task-syntax.yaml"></a>

```
Type: AWS::DataSync::Task
Properties: 
  [CloudWatchLogGroupArn](#cfn-datasync-task-cloudwatchloggrouparn): String
  [DestinationLocationArn](#cfn-datasync-task-destinationlocationarn): String
  [Excludes](#cfn-datasync-task-excludes): 
    - FilterRule
  [Includes](#cfn-datasync-task-includes): 
    - FilterRule
  [Name](#cfn-datasync-task-name): String
  [Options](#cfn-datasync-task-options): 
    Options
  [Schedule](#cfn-datasync-task-schedule): 
    TaskSchedule
  [SourceLocationArn](#cfn-datasync-task-sourcelocationarn): String
  [Tags](#cfn-datasync-task-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-task-properties"></a>

`CloudWatchLogGroupArn`  <a name="cfn-datasync-task-cloudwatchloggrouparn"></a>
The Amazon Resource Name \(ARN\) of the Amazon CloudWatch log group that is used to monitor and log events in the task\.   
For more information about how to use CloudWatch Logs with DataSync, see [Monitoring Your Task](https://docs.aws.amazon.com/datasync/latest/userguide/monitor-datasync.html#cloudwatchlogs) in the * AWS DataSync User Guide\.*   
For more information about these groups, see [Working with Log Groups and Log Streams](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/Working-with-log-groups-and-streams.html) in the *Amazon CloudWatch Logs User Guide*\.  
*Required*: No  
*Type*: String  
*Maximum*: `562`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):logs:[a-z\-0-9]*:[0-9]{12}:log-group:([^:\*]*)(:\*)?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationLocationArn`  <a name="cfn-datasync-task-destinationlocationarn"></a>
The Amazon Resource Name \(ARN\) of an AWS storage resource's location\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Excludes`  <a name="cfn-datasync-task-excludes"></a>
A list of filter rules that determines which files to exclude from a task\. The list should contain a single filter string that consists of the patterns to exclude\. The patterns are delimited by "\|" \(that is, a pipe\), for example, `"/folder1|/folder2"`\.   
   
*Required*: No  
*Type*: List of [FilterRule](aws-properties-datasync-task-filterrule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Includes`  <a name="cfn-datasync-task-includes"></a>
A list of filter rules that determines which files to include when running a task\. The pattern contains a single filter string that consists of the patterns to include\. The patterns are delimited by "\|" \(that is, a pipe\), for example, `"/folder1|/folder2"`\.  
*Required*: No  
*Type*: List of [FilterRule](aws-properties-datasync-task-filterrule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-datasync-task-name"></a>
The name of a task\. This value is a text reference that is used to identify the task in the console\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9\s+=._:@/-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-datasync-task-options"></a>
The set of configuration options that control the behavior of a single execution of the task that occurs when you call `StartTaskExecution`\. You can configure these options to preserve metadata such as user ID \(UID\) and group ID \(GID\), file permissions, data integrity verification, and so on\.  
For each individual task execution, you can override these options by specifying the `OverrideOptions` before starting the task execution\. For more information, see the [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html) operation\.   
*Required*: No  
*Type*: [Options](aws-properties-datasync-task-options.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-datasync-task-schedule"></a>
Specifies a schedule used to periodically transfer files from a source to a destination location\. The schedule should be specified in UTC time\. For more information, see [Scheduling your task](https://docs.aws.amazon.com/datasync/latest/userguide/task-scheduling.html)\.  
*Required*: No  
*Type*: [TaskSchedule](aws-properties-datasync-task-taskschedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceLocationArn`  <a name="cfn-datasync-task-sourcelocationarn"></a>
The Amazon Resource Name \(ARN\) of the source location for the task\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):datasync:[a-z\-0-9]+:[0-9]{12}:location/loc-[0-9a-z]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-task-tags"></a>
The key\-value pair that represents the tag that you want to add to the resource\. The value can be an empty string\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-task-return-values"></a>

### Ref<a name="aws-resource-datasync-task-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-task-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-task-return-values-fn--getatt-fn--getatt"></a>

`DestinationNetworkInterfaceArns`  <a name="DestinationNetworkInterfaceArns-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ErrorCode`  <a name="ErrorCode-fn::getatt"></a>
Errors that AWS DataSync encountered during execution of the task\. You can use this error code to help troubleshoot issues\.

`ErrorDetail`  <a name="ErrorDetail-fn::getatt"></a>
Detailed description of an error that was encountered during the task execution\. You can use this information to help troubleshoot issues\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the task that was described\.

`TaskArn`  <a name="TaskArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the task\.

## Examples<a name="aws-resource-datasync-task--examples"></a>



### DataSync Task<a name="aws-resource-datasync-task--examples--DataSync_Task"></a>

The following example specifies a DataSync task using a source and destination location\. 

#### JSON<a name="aws-resource-datasync-task--examples--DataSync_Task--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies a DataSync task",
"Resources": 
  {
  "Agent": {
    "Type": "AWS::DataSync::Task",
    "Properties": {
      "SourceLocationArn": "arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3",
      "DestinationLocationArn": "arn:aws:datasync:us-east-2:111222333444:location/loc-18ec8bcgd437d61t4"
    }
  }
}
```

#### YAML<a name="aws-resource-datasync-task--examples--DataSync_Task--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a DataSync task
Resources:
  Task:
    Type: AWS::DataSync::Task
    Properties:
      SourceLocationArn: arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3
      DestinationLocationArn: arn:aws:datasync:us-east-2:111222333444:location/loc-18ec8bcgd437d61t4
```