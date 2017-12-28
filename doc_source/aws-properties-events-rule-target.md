# Amazon CloudWatch Events Rule Target<a name="aws-properties-events-rule-target"></a>

The `Target` property type specifies a target, such as AWS Lambda \(Lambda\) functions or Kinesis streams, that CloudWatch Events invokes when a rule is triggered\.

The `Targets` property of the [AWS::Events::Rule](aws-resource-events-rule.md) resource contains a list of one or more `Target` property types\.

## Syntax<a name="w3ab2c21c14d282b7"></a>

### JSON<a name="aws-properties-events-rule-target-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-arn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-ecsparameters)" : EcsParameters,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-input)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-inputpath)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-inputtransformer)" : InputTransformer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-kinesisparameters)" : KinesisParameters,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-rolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-runcommandparameters)" : RunCommandParameters
}
```

### YAML<a name="aws-properties-events-rule-target-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-arn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-ecsparameters):
  EcsParameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-input): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-inputpath): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-inputtransformer):
  InputTransformer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-kinesisparameters):
  KinesisParameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-target-runcommandparameters):
  RunCommandParameters
```

## Properties<a name="w3ab2c21c14d282b9"></a>

**Note**  
For more information about each property, including constraints and valid values, see [Amazon CloudWatch Events Rule Target](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_Target.html) in the *Amazon CloudWatch Events API Reference*\.

`Arn`  
The Amazon Resource Name \(ARN\) of the target\.  
*Required: *Yes  
*Type*: String

`EcsParameters`  
The Amazon ECS task definition and task count to use, if the event target is an Amazon ECS task\.  
 *Required*: No  
 *Type*: [CloudWatch Events Rule EcsParameters](aws-properties-events-rule-ecsparameters.md)

`Id`  
A unique, user\-defined identifier for the target\. Acceptable values include alphanumeric characters, periods \(`.`\), hyphens \(`-`\), and underscores \(`_`\)\.  
*Required: *Yes  
*Type*: String

`Input`  
A JSON\-formatted text string that is passed to the target\. This value overrides the matched event\.  
*Required: *No\. If you don't specify both this property and the `InputPath` property, CloudWatch Events passes the entire matched event to the target\.  
*Type*: String

`InputPath`  
When you don't want to pass the entire matched event, the JSONPath that describes which part of the event to pass to the target\.  
*Required: *No\. If you don't specify both this property and the `Input` property, CloudWatch Events passes the entire matched event to the target\.  
*Type*: String

`InputTransformer`  
Settings that provide custom input to a target based on certain event data\. You can extract one or more key\-value pairs from the event, and then use that data to send customized input to the target\.  
 *Required*: No  
 *Type*: [CloudWatch Events Rule InputTransformer](aws-properties-events-rule-inputtransformer.md)

`KinesisParameters`  
Settings that control shard assignment, when the target is a Kinesis stream\. If you don't include this parameter, `eventId` is used as the partition key\.  
 *Required*: No  
 *Type*: [CloudWatch Events Rule KinesisParameters](aws-properties-events-rule-kinesisparameters.md)

`RoleArn`  
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role to use for this target when the rule is triggered\. If one rule triggers multiple targets, you can use a different IAM role for each target\.  
CloudWatch Events needs appropriate permissions to make API calls against the resources you own\. For Kinesis streams, CloudWatch Events relies on IAM roles\. For Lambda, Amazon SNS, and Amazon SQS resources, CloudWatch Events relies on resource\-based policies\. For more information, see [ Using Resource\-Based Policies for CloudWatch Events](http://docs.aws.amazon.com/AmazonCloudWatch/latest/events/resource-based-policies-cwe.html) in the *Amazon CloudWatch User Guide*\.
*Required: *No  
*Type*: String

`RunCommandParameters`  
Parameters used when the rule invokes Amazon EC2 Systems Manager Run Command\.  
 *Required*: No  
 *Type*: [CloudWatch Events Rule RunCommandParameters](aws-properties-events-rule-runcommandparameters.md)

## Examples<a name="aws-properties-events-rule-target-examples"></a>

The following examples define targets for an `AWS::Events::Rule` resource\. For more examples, see [ PutTargets](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutTargets.html#API_PutTargets_Examples) in the *Amazon CloudWatch Events API Reference*\.

### Target with `KinesisParameters`<a name="aws-properties-events-rule-target-example1"></a>

The following snippet creates a Kinesis stream target\.

#### JSON<a name="aws-properties-events-rule-target-example1.json"></a>

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

#### YAML<a name="aws-properties-events-rule-target-example1.yaml"></a>

```
MyEventsRule:
  Type: 'AWS::Events::Rule'
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

### Target with `EcsParameters`<a name="aws-properties-events-rule-target-example2"></a>

The following snippet creates an Amazon ECS task target\.

#### JSON<a name="aws-properties-events-rule-target-example2.json"></a>

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

#### YAML<a name="aws-properties-events-rule-target-example2.yaml"></a>

```
MyEventsRule:
  Type: 'AWS::Events::Rule'
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