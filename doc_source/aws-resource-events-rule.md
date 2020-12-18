# AWS::Events::Rule<a name="aws-resource-events-rule"></a>

The `AWS::Events::Rule` resource creates a rule that matches incoming events and routes them to one or more targets for processing\. For more information, see [What Is Amazon Eventbridge?](https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html)\. 

A rule must contain at least one `EventPattern` or `ScheduleExpression`\. Rules with `EventPattern` are triggered when a matching event is observed\. Rules with `ScheduleExpression` self\-trigger based on the given schedule\. A rule can have both an `EventPattern` and a `ScheduleExpression`, in which case the rule triggers on matching events as well as on a schedule\.

Most services in AWS treat `:` or `/` as the same character in Amazon Resource Names \(ARNs\)\. However, EventBridge uses an exact match in event patterns and rules\. Be sure to use the correct ARN characters when creating event patterns so that they match the ARN syntax in the event that you want to match\.

## Syntax<a name="aws-resource-events-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-rule-syntax.json"></a>

```
{
  "Type" : "AWS::Events::Rule",
  "Properties" : {
      "[Description](#cfn-events-rule-description)" : String,
      "[EventBusName](#cfn-events-rule-eventbusname)" : String,
      "[EventPattern](#cfn-events-rule-eventpattern)" : Json,
      "[Name](#cfn-events-rule-name)" : String,
      "[RoleArn](#cfn-events-rule-rolearn)" : String,
      "[ScheduleExpression](#cfn-events-rule-scheduleexpression)" : String,
      "[State](#cfn-events-rule-state)" : String,
      "[Targets](#cfn-events-rule-targets)" : [ Target, ... ]
    }
}
```

### YAML<a name="aws-resource-events-rule-syntax.yaml"></a>

```
Type: AWS::Events::Rule
Properties: 
  [Description](#cfn-events-rule-description): String
  [EventBusName](#cfn-events-rule-eventbusname): String
  [EventPattern](#cfn-events-rule-eventpattern): Json
  [Name](#cfn-events-rule-name): String
  [RoleArn](#cfn-events-rule-rolearn): String
  [ScheduleExpression](#cfn-events-rule-scheduleexpression): String
  [State](#cfn-events-rule-state): String
  [Targets](#cfn-events-rule-targets): 
    - Target
```

## Properties<a name="aws-resource-events-rule-properties"></a>

`Description`  <a name="cfn-events-rule-description"></a>
The description of the rule\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBusName`  <a name="cfn-events-rule-eventbusname"></a>
The event bus name or ARN to associate with this rule\. If you omit this, the default event bus is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[/\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventPattern`  <a name="cfn-events-rule-eventpattern"></a>
Describes which events are routed to the specified target\. For more information, see [Events and Event Patterns in EventBridge](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-and-event-patterns.html) in the *Amazon EventBridge User Guide*\.  
When using CloudFormation, you must enclose each part of the event pattern in square brackets, as follows:  
`"EventPattern": { "source": [ "aws.ec2" ], "detail-type": [ "EC2 Instance State-change Notification" ] }`  
To create a rule, you must include at least one `EventPattern` or `ScheduleExpression`\. You can create a rule that includes both\.  
*Required*: Conditional  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-events-rule-name"></a>
The name of the rule\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the rule name\.   
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-events-rule-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that is used for target invocation\.  
If you're setting an event bus in another account as the target and that account granted permission to your account through an organization instead of directly by the account ID, you must specify a `RoleArn` with proper permissions in the `Target` structure, instead of here in this parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-events-rule-scheduleexpression"></a>
The scheduling expression that determines when and how often the rule runs\. For more information, see [Schedule Expressions for Rules](https://docs.aws.amazon.com/eventbridge/latest/userguide/scheduled-events.html)\.  
A rule must contain either `ScheduleExpression` or `EventPattern`\.  
*Required*: Conditional  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-events-rule-state"></a>
Indicates whether the rule is enabled\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-events-rule-targets"></a>
The AWS resources that are invoked when the rule is triggered\. For information about valid targets, see [PutTargets](https://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutTargets.html)\.  
If you're setting the event bus of another account as the target and that account granted permission to your account through an organization instead of directly by the account ID, you must specify a `RoleArn` with proper permissions in the `Target` structure\. For more information, see [Sending and Receiving Events Between AWS Accounts](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-cross-account-event-delivery.html) in the *Amazon EventBridge User Guide*\.  
To learn more using a dead\-letter queue to send events that fail to be delivered to a target, see [Event retry policy and using dead\-letter queues](https://docs.aws.amazon.com/eventbridge/latest/userguide/rule-dlq.html)\.  
*Required*: No  
*Type*: List of [Target](aws-properties-events-rule-target.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-events-rule-return-values"></a>

### Ref<a name="aws-resource-events-rule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns event rule ID, such as `mystack-ScheduledRule-ABCDEFGHIJK`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-events-rule-return-values-fn--getatt"></a>

#### <a name="aws-resource-events-rule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the rule, such as `arn:aws:events:us-east-2:123456789012:rule/example`\.

## Examples<a name="aws-resource-events-rule--examples"></a>



### Create a rule that includes a dead\-letter queue for a target<a name="aws-resource-events-rule--examples--Create_a_rule_that_includes_a_dead-letter_queue_for_a_target"></a>

The following example demonstrates how to send all EC2 events to an SQS queue, and include a dead\-letter queue and retry policy settings for the target of the rule\.

#### JSON<a name="aws-resource-events-rule--examples--Create_a_rule_that_includes_a_dead-letter_queue_for_a_target--json"></a>

```
{
   "MyNewEventsRule": {
      "Type": "AWS::Events::Rule",
      "Properties": {
         "Description": "Test Events Rule",
         "Name": "mynewabc",
         "EventPattern": {
            "source": [
               "aws.ec2"
            ]
         },
         "State": "ENABLED",
         "Targets": [
            {
               "Arn": "arn:aws:sqs:us-west-2:081035103721:demoSQS",
               "Id": "Id1234",
               "RetryPolicy": {
                  "MaximumRetryAttempts": 4,
                  "MaximumEventAgeInSeconds": 400
               },
               "DeadLetterConfig": {
                  "Arn": "arn:aws:sqs:us-west-2:081035103721:demoDLQ"
               }
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-events-rule--examples--Create_a_rule_that_includes_a_dead-letter_queue_for_a_target--yaml"></a>

```
MyNewEventsRule:
  Type: 'AWS::Events::Rule'
  Properties:
    Description: Test Events Rule
    Name: mynewabc
    EventPattern:
      source:
        - aws.ec2
    State: ENABLED
    Targets:
      - Arn: 'arn:aws:sqs:us-west-2:081035103721:demoSQS'
        Id: Id1234
        RetryPolicy:
          MaximumRetryAttempts: 4
          MaximumEventAgeInSeconds: 400
        DeadLetterConfig:
          Arn: 'arn:aws:sqs:us-west-2:081035103721:demoDLQ'
```

### Regularly invoke Lambda function<a name="aws-resource-events-rule--examples--Regularly_invoke_Lambda_function"></a>

The following example creates a rule that invokes the specified Lambda function every 10 minutes\. The `PermissionForEventsToInvokeLambda` resource grants EventBridge permission to invoke the associated function\. 

#### JSON<a name="aws-resource-events-rule--examples--Regularly_invoke_Lambda_function--json"></a>

```
"ScheduledRule": {
  "Type": "AWS::Events::Rule",
  "Properties": {
    "Description": "ScheduledRule",
    "ScheduleExpression": "rate(10 minutes)",
    "State": "ENABLED",
    "Targets": [{
      "Arn": { "Fn::GetAtt": ["LambdaFunction", "Arn"] },
      "Id": "TargetFunctionV1"
    }]
  }
},
"PermissionForEventsToInvokeLambda": {
  "Type": "AWS::Lambda::Permission",
  "Properties": {
    "FunctionName": { "Ref": "LambdaFunction" },
    "Action": "lambda:InvokeFunction",
    "Principal": "events.amazonaws.com",
    "SourceArn": { "Fn::GetAtt": ["ScheduledRule", "Arn"] }
  }
}
```

#### YAML<a name="aws-resource-events-rule--examples--Regularly_invoke_Lambda_function--yaml"></a>

```
ScheduledRule: 
  Type: AWS::Events::Rule
  Properties: 
    Description: "ScheduledRule"
    ScheduleExpression: "rate(10 minutes)"
    State: "ENABLED"
    Targets: 
      - 
        Arn: 
          Fn::GetAtt: 
            - "LambdaFunction"
            - "Arn"
        Id: "TargetFunctionV1"
PermissionForEventsToInvokeLambda: 
  Type: AWS::Lambda::Permission
  Properties: 
    FunctionName: !Ref "LambdaFunction"
    Action: "lambda:InvokeFunction"
    Principal: "events.amazonaws.com"
    SourceArn: 
      Fn::GetAtt: 
        - "ScheduledRule"
        - "Arn"
```

### Invoke Lambda Function in Response to an Event<a name="aws-resource-events-rule--examples--Invoke_Lambda_Function_in_Response_to_an_Event"></a>

The following example creates a rule that invokes the specified Lambda function when any EC2 instance's state changes to stopping\.

#### JSON<a name="aws-resource-events-rule--examples--Invoke_Lambda_Function_in_Response_to_an_Event--json"></a>

```
"EventRule": {
  "Type": "AWS::Events::Rule",
  "Properties": {
    "Description": "EventRule",
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
    "State": "ENABLED",
    "Targets": [{
      "Arn": { "Fn::GetAtt": ["LambdaFunction", "Arn"] },
      "Id": "TargetFunctionV1"
    }]
  }
},
"PermissionForEventsToInvokeLambda": {
  "Type": "AWS::Lambda::Permission",
  "Properties": {
    "FunctionName": { "Ref": "LambdaFunction" },
    "Action": "lambda:InvokeFunction",
    "Principal": "events.amazonaws.com",
    "SourceArn": { "Fn::GetAtt": ["EventRule", "Arn"] }
  }
}
```

#### YAML<a name="aws-resource-events-rule--examples--Invoke_Lambda_Function_in_Response_to_an_Event--yaml"></a>

```
EventRule: 
  Type: AWS::Events::Rule
  Properties: 
    Description: "EventRule"
    EventPattern: 
      source: 
        - "aws.ec2"
      detail-type: 
        - "EC2 Instance State-change Notification"
      detail: 
        state: 
          - "stopping"
    State: "ENABLED"
    Targets: 
      - 
        Arn: 
          Fn::GetAtt: 
            - "LambdaFunction"
            - "Arn"
        Id: "TargetFunctionV1"
PermissionForEventsToInvokeLambda: 
  Type: AWS::Lambda::Permission
  Properties: 
    FunctionName: 
      Ref: "LambdaFunction"
    Action: "lambda:InvokeFunction"
    Principal: "events.amazonaws.com"
    SourceArn: 
      Fn::GetAtt: 
        - "EventRule"
        - "Arn"
```

### Notify a Topic in Response to a Log Entry<a name="aws-resource-events-rule--examples--Notify_a_Topic_in_Response_to_a_Log_Entry"></a>

The following example creates a rule that notifies an Amazon Simple Notification Service topic if an AWS CloudTrail log entry contains a call by the Root user\. The `EventTopicPolicy ` resource grants Amazon EventBridge permission to notify the associated Amazon SNS topic\. 

#### JSON<a name="aws-resource-events-rule--examples--Notify_a_Topic_in_Response_to_a_Log_Entry--json"></a>

```
"OpsEventRule": {
  "Type": "AWS::Events::Rule",
  "Properties": {
    "Description": "EventRule",
    "EventPattern": {
      "detail-type": [ "AWS API Call via CloudTrail" ],
      "detail": { 
        "userIdentity": { 
          "type": [ "Root" ]
        }
      }
    },
    "State": "ENABLED",
    "Targets": [
      {
        "Arn": { "Ref": "MySNSTopic" },
        "Id": "OpsTopic"
      }
    ]
  }
}
"EventTopicPolicy": {
  "Type": "AWS::SNS::TopicPolicy",
  "Properties": {
    "PolicyDocument": {
      "Statement": [
        {
          "Effect": "Allow",
          "Principal": { "Service": "events.amazonaws.com" },
          "Action": "sns:Publish",
          "Resource": "*"
        }
      ]
    },
    "Topics": [ { "Ref": "MySNSTopic" } ]
  }
}
```

#### YAML<a name="aws-resource-events-rule--examples--Notify_a_Topic_in_Response_to_a_Log_Entry--yaml"></a>

```
OpsEventRule: 
  Type: AWS::Events::Rule
  Properties: 
    Description: "EventRule"
    EventPattern: 
      detail-type: 
        - "AWS API Call via CloudTrail"
      detail: 
        userIdentity: 
          type: 
            - "Root"
    State: "ENABLED"
    Targets: 
      - 
        Arn: 
          Ref: "MySNSTopic"
        Id: "OpsTopic"
EventTopicPolicy:
  Type: 'AWS::SNS::TopicPolicy'
  Properties:
    PolicyDocument:
      Statement:
        - Effect: Allow
          Principal:
            Service: events.amazonaws.com
          Action: 'sns:Publish'
          Resource: '*'
    Topics:
      - !Ref MySNSTopic
```