# AWS::Events::Rule Target<a name="aws-properties-events-rule-target"></a>

Targets are the resources to be invoked when a rule is triggered\. For a complete list of services and resources that can be set as a target, see [PutTargets](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutTargets.html)\.

If you are setting the event bus of another account as the target, and that account granted permission to your account through an organization instead of directly by the account ID, then you must specify a `RoleArn` with proper permissions in the `Target` structure\. For more information, see [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-cross-account-event-delivery.html) in the *Amazon EventBridge User Guide*\.

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
  "[SageMakerPipelineParameters](#cfn-events-rule-target-sagemakerpipelineparameters)" : SageMakerPipelineParameters,
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
  [SageMakerPipelineParameters](#cfn-events-rule-target-sagemakerpipelineparameters): 
    SageMakerPipelineParameters
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
If the event target is an AWS Batch job, this contains the job definition, job name, and other parameters\. For more information, see [Jobs](https://docs.aws.amazon.com/batch/latest/userguide/jobs.html) in the * AWS Batch User Guide*\.  
*Required*: No  
*Type*: [BatchParameters](aws-properties-events-rule-batchparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-events-rule-target-deadletterconfig"></a>
The `DeadLetterConfig` that defines the target queue to send dead\-letter queue events to\.  
*Required*: No  
*Type*: [DeadLetterConfig](aws-properties-events-rule-deadletterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcsParameters`  <a name="cfn-events-rule-target-ecsparameters"></a>
Contains the Amazon ECS task definition and task count to be used, if the event target is an Amazon ECS task\. For more information about Amazon ECS tasks, see [Task Definitions ](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_defintions.html) in the *Amazon EC2 Container Service Developer Guide*\.  
*Required*: No  
*Type*: [EcsParameters](aws-properties-events-rule-ecsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpParameters`  <a name="cfn-events-rule-target-httpparameters"></a>
Contains the HTTP parameters to use when the target is a API Gateway endpoint or EventBridge ApiDestination\.  
If you specify an API Gateway API or EventBridge ApiDestination as a target, you can use this parameter to specify headers, path parameters, and query string keys/values as part of your target invoking request\. If you're using ApiDestinations, the corresponding Connection can also have these values configured\. In case of any conflicting keys, values from the Connection take precedence\.  
*Required*: No  
*Type*: [HttpParameters](aws-properties-events-rule-httpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-events-rule-target-id"></a>
The ID of the target within the specified rule\. Use this ID to reference the target when updating the rule\. We recommend using a memorable and unique string\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Input`  <a name="cfn-events-rule-target-input"></a>
Valid JSON text passed to the target\. In this case, nothing from the event itself is passed to the target\. For more information, see [The JavaScript Object Notation \(JSON\) Data Interchange Format](http://www.rfc-editor.org/rfc/rfc7159.txt)\.  
*Required*: No  
*Type*: String  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputPath`  <a name="cfn-events-rule-target-inputpath"></a>
The value of the JSONPath that is used for extracting part of the matched event when passing it to the target\. You may use JSON dot notation or bracket notation\. For more information about JSON paths, see [JSONPath](http://goessner.net/articles/JsonPath/)\.  
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
Contains the Amazon Redshift Data API parameters to use when the target is a Amazon Redshift cluster\.  
If you specify a Amazon Redshift Cluster as a Target, you can use this to specify parameters to invoke the Amazon Redshift Data API ExecuteStatement based on EventBridge events\.  
*Required*: No  
*Type*: [RedshiftDataParameters](aws-properties-events-rule-redshiftdataparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-events-rule-target-retrypolicy"></a>
The `RetryPolicy` object that contains the retry policy configuration to use for the dead\-letter queue\.  
*Required*: No  
*Type*: [RetryPolicy](aws-properties-events-rule-retrypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-events-rule-target-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to be used for this target when the rule is triggered\. If one rule triggers multiple targets, you can use a different IAM role for each target\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunCommandParameters`  <a name="cfn-events-rule-target-runcommandparameters"></a>
Parameters used when you are using the rule to invoke Amazon EC2 Run Command\.  
*Required*: No  
*Type*: [RunCommandParameters](aws-properties-events-rule-runcommandparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SageMakerPipelineParameters`  <a name="cfn-events-rule-target-sagemakerpipelineparameters"></a>
Contains the SageMaker Model Building Pipeline parameters to start execution of a SageMaker Model Building Pipeline\.  
If you specify a SageMaker Model Building Pipeline as a target, you can use this to specify parameters to start a pipeline execution based on EventBridge events\.  
*Required*: No  
*Type*: [SageMakerPipelineParameters](aws-properties-events-rule-sagemakerpipelineparameters.md)  
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