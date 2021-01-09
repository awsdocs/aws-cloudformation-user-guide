# AWS::Events::Rule Target<a name="aws-properties-events-rule-target"></a>

The `Target` property type specifies a target, such as an AWS Lambda function or an Amazon Kinesis data stream, that EventBridge invokes when a rule is triggered\. 

The `Targets` property of the [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html) resource contains a list of one or more `Target` property types\.

## Syntax<a name="aws-properties-events-rule-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-target-syntax.json"></a>

```
{
  "[Arn](#cfn-events-rule-target-arn)" : String,
  "[BatchParameters](#cfn-events-rule-target-batchparameters)" : BatchParameters,
  "[DeadLetterConfig](#cfn-events-rule-target-deadletterconfig)" : DeadLetterConfig,
  "[EcsParameters](#cfn-events-rule-target-ecsparameters)" : EcsParameters,
  "[HttpParameters](#cfn-events-rule-target-httpparameters)" : HttpParameters,
  "[Id](#cfn-events-rule-target-id)" : String,
  "[Input](#cfn-events-rule-target-input)" : String,
  "[InputPath](#cfn-events-rule-target-inputpath)" : String,
  "[InputTransformer](#cfn-events-rule-target-inputtransformer)" : InputTransformer,
  "[KinesisParameters](#cfn-events-rule-target-kinesisparameters)" : KinesisParameters,
  "[RedshiftDataParameters](#cfn-events-rule-target-redshiftdataparameters)" : RedshiftDataParameters,
  "[RetryPolicy](#cfn-events-rule-target-retrypolicy)" : RetryPolicy,
  "[RoleArn](#cfn-events-rule-target-rolearn)" : String,
  "[RunCommandParameters](#cfn-events-rule-target-runcommandparameters)" : RunCommandParameters,
  "[SqsParameters](#cfn-events-rule-target-sqsparameters)" : SqsParameters
}
```

### YAML<a name="aws-properties-events-rule-target-syntax.yaml"></a>

```
  [Arn](#cfn-events-rule-target-arn): String
  [BatchParameters](#cfn-events-rule-target-batchparameters): 
    BatchParameters
  [DeadLetterConfig](#cfn-events-rule-target-deadletterconfig): 
    DeadLetterConfig
  [EcsParameters](#cfn-events-rule-target-ecsparameters): 
    EcsParameters
  [HttpParameters](#cfn-events-rule-target-httpparameters): 
    HttpParameters
  [Id](#cfn-events-rule-target-id): String
  [Input](#cfn-events-rule-target-input): String
  [InputPath](#cfn-events-rule-target-inputpath): String
  [InputTransformer](#cfn-events-rule-target-inputtransformer): 
    InputTransformer
  [KinesisParameters](#cfn-events-rule-target-kinesisparameters): 
    KinesisParameters
  [RedshiftDataParameters](#cfn-events-rule-target-redshiftdataparameters): 
    RedshiftDataParameters
  [RetryPolicy](#cfn-events-rule-target-retrypolicy): 
    RetryPolicy
  [RoleArn](#cfn-events-rule-target-rolearn): String
  [RunCommandParameters](#cfn-events-rule-target-runcommandparameters): 
    RunCommandParameters
  [SqsParameters](#cfn-events-rule-target-sqsparameters): 
    SqsParameters
```

## Properties<a name="aws-properties-events-rule-target-properties"></a>

`Arn`  <a name="cfn-events-rule-target-arn"></a>
The Amazon Resource Name \(ARN\) of the target\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BatchParameters`  <a name="cfn-events-rule-target-batchparameters"></a>
If the event target is an AWS Batch job, this contains the job definition, job name, and other parameters\. For more information, see [Jobs](https://docs.aws.amazon.com/batch/latest/userguide/jobs.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: [BatchParameters](aws-properties-events-rule-batchparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-events-rule-target-deadletterconfig"></a>
The `DeadLetterConfig` that defines the target queue to send dead\-letter queue events to\.   
To learn more using a dead\-letter queue to send events that fail to be delivered to a target, see [Event retry policy and using dead\-letter queues](https://docs.aws.amazon.com/eventbridge/latest/userguide/rule-dlq.html)\.  
*Required*: No  
*Type*: [DeadLetterConfig](aws-properties-events-rule-deadletterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcsParameters`  <a name="cfn-events-rule-target-ecsparameters"></a>
Contains the Amazon ECS task definition and task count to be used, if the event target is an Amazon ECS task\. For more information about Amazon ECS tasks, see [Task Definitions ](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_defintions.html) in the *Amazon EC2 Container Service Developer Guide*\.  
*Required*: No  
*Type*: [EcsParameters](aws-properties-events-rule-ecsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpParameters`  <a name="cfn-events-rule-target-httpparameters"></a>
Contains the HTTP parameters to use when the target is a API Gateway REST endpoint\.  
If you specify an API Gateway REST API as a target, you can use this parameter to specify headers, path parameter, query string keys/values as part of your target invoking request\.  
*Required*: No  
*Type*: [HttpParameters](aws-properties-events-rule-httpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-events-rule-target-id"></a>
A name for the target\. Use a string that will help you identify the target\. Each target associated with a rule must have an Id unique for that rule\.  
The `Id` can include alphanumeric characters, periods \(\.\), hyphens \(\-\), and underscores \(\_\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Input`  <a name="cfn-events-rule-target-input"></a>
Valid JSON text passed to the target\. If you use this property, nothing from the event text itself is passed to the target\.  
*Required*: No  
*Type*: String  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputPath`  <a name="cfn-events-rule-target-inputpath"></a>
When you don't want to pass the entire matched event, `InputPath ` describes which part of the event to pass to the target\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputTransformer`  <a name="cfn-events-rule-target-inputtransformer"></a>
Settings to enable you to provide custom input to a target based on certain event data\. You can extract one or more key\-value pairs from the event and then use that data to send customized input to the target\.  
*Required*: No  
*Type*: [InputTransformer](aws-properties-events-rule-inputtransformer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisParameters`  <a name="cfn-events-rule-target-kinesisparameters"></a>
The custom parameter you can use to control the shard assignment, when the target is a Kinesis data stream\. If you do not include this parameter, the default is to use the `eventId` as the partition key\.  
*Required*: No  
*Type*: [KinesisParameters](aws-properties-events-rule-kinesisparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftDataParameters`  <a name="cfn-events-rule-target-redshiftdataparameters"></a>
Contains the Redshift Data API parameters to use when the target is a Redshift cluster\.  
If you specify a Redshift Cluster as a Target, you can use this to specify parameters to invoke the Redshift Data API ExecuteStatement based on EventBridge events\.  
*Required*: No  
*Type*: [RedshiftDataParameters](aws-properties-events-rule-redshiftdataparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-events-rule-target-retrypolicy"></a>
A `RetryPolicy` object that includes information about the retry policy settings\.  
To learn more using retry policy settings and using dead\-letter queues, see [Event retry policy and using dead\-letter queues](https://docs.aws.amazon.com/eventbridge/latest/userguide/rule-dlq.html)\.  
*Required*: No  
*Type*: [RetryPolicy](aws-properties-events-rule-retrypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-events-rule-target-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to be used for this target when the rule is triggered\. If one rule triggers multiple targets, you can use a different IAM role for each target\.  
If you're setting an event bus in another account as the target and that account granted permission to your account through an organization instead of directly by the account ID, you must specify a `RoleArn` with proper permissions here in this parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunCommandParameters`  <a name="cfn-events-rule-target-runcommandparameters"></a>
Parameters used when you are using the rule to invoke Amazon EC2 Run Command\.  
*Required*: No  
*Type*: [RunCommandParameters](aws-properties-events-rule-runcommandparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqsParameters`  <a name="cfn-events-rule-target-sqsparameters"></a>
Contains the message group ID to use when the target is a FIFO queue\.  
If you specify an SQS FIFO queue as a target, the queue must have content\-based deduplication enabled\.  
*Required*: No  
*Type*: [SqsParameters](aws-properties-events-rule-sqsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-events-rule-target--examples"></a>



### Target with KinesisParameters<a name="aws-properties-events-rule-target--examples--Target_with_KinesisParameters"></a>

The following snippet creates a Kinesis data stream target\.

#### JSON<a name="aws-properties-events-rule-target--examples--Target_with_KinesisParameters--json"></a>

```
"MyEventsRule": {
    "Type": "AWS::Events::Rule",
    "Properties": {
        "Description": "Events Rule with KinesisParameters",
        "EventPattern": {
            "source": [
                "aws.ec2"
            ]
        },
        "RoleArn": {
            "Fn::GetAtt": [
                "EventsInvokeKinesisTargetRole",
                "Arn"
            ]
        },
        "ScheduleExpression": "rate(5 minutes)",
        "State": "ENABLED",
        "Targets": [
            {
                "Arn": {
                    "Fn::GetAtt": [
                        "MyFirstStream",
                        "Arn"
                    ]
                },
                "Id": "Id123",
                "RoleArn": {
                    "Fn::GetAtt": [
                        "EventsInvokeKinesisTargetRole",
                        "Arn"
                    ]
                },
                "KinesisParameters": {
                    "PartitionKeyPath": "$"
                }
            }
        ]
    }
}
```

#### YAML<a name="aws-properties-events-rule-target--examples--Target_with_KinesisParameters--yaml"></a>

```
MyEventsRule:
  Type: AWS::Events::Rule
  Properties:
    Description: Events Rule with KinesisParameters
    EventPattern:
      source:
        - aws.ec2
    RoleArn: !GetAtt 
      - EventsInvokeKinesisTargetRole
      - Arn
    ScheduleExpression: rate(5 minutes)
    State: ENABLED
    Targets:
      - Arn: !GetAtt 
          - MyFirstStream
          - Arn
        Id: Id123
        RoleArn: !GetAtt 
          - EventsInvokeKinesisTargetRole
          - Arn
        KinesisParameters:
          PartitionKeyPath: $
```

### Target with EcsParameters<a name="aws-properties-events-rule-target--examples--Target_with_EcsParameters"></a>

The following snippet creates an Amazon ECS task target\.

#### JSON<a name="aws-properties-events-rule-target--examples--Target_with_EcsParameters--json"></a>

```
"MyEventsRule": {
  "Type": "AWS::Events::Rule",
  "Properties": {
      "Description": "Events Rule with EcsParameters",
      "EventPattern": {
          "source": [
              "aws.ec2"
          ],
          "detail-type": [
              "EC2 Instance State-change Notification"
          ],
          "detail": {
              "state": [
                  "stopping"
              ]
          }
      },
      "ScheduleExpression": "rate(15 minutes)",
      "State": "DISABLED",
      "Targets": [
          {
              "Arn": {
                  "Fn::GetAtt": [
                      "MyCluster",
                      "Arn"
                  ]
              },
              "RoleArn": {
                  "Fn::GetAtt": [
                      "ECSTaskRole",
                      "Arn"
                  ]
              },
              "Id": "Id345",
              "EcsParameters": {
                  "TaskCount": 1,
                  "TaskDefinitionArn": {
                      "Ref": "MyECSTask"
                  }
              }
          }
      ]
  }
}
```

#### YAML<a name="aws-properties-events-rule-target--examples--Target_with_EcsParameters--yaml"></a>

```
MyEventsRule:
  Type: AWS::Events::Rule
  Properties:
    Description: Events Rule with EcsParameters
    EventPattern:
      source:
        - aws.ec2
      detail-type:
        - EC2 Instance State-change Notification
      detail:
        state:
          - stopping
    ScheduleExpression: rate(15 minutes)
    State: DISABLED
    Targets:
      - Arn: !GetAtt 
          - MyCluster
          - Arn
        RoleArn: !GetAtt 
          - ECSTaskRole
          - Arn
        Id: Id345
        EcsParameters:
          TaskCount: 1
          TaskDefinitionArn: !Ref MyECSTask
```