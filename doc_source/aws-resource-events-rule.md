# AWS::Events::Rule<a name="aws-resource-events-rule"></a>

The `AWS::Events::Rule` resource creates a rule that matches incoming Amazon CloudWatch Events \(CloudWatch Events\) events and routes them to one or more targets for processing\. For more information, see [Using CloudWatch Events](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/WhatIsCloudWatchEvents.html) in the *Amazon CloudWatch User Guide*\.

**Topics**
+ [Syntax](#aws-resource-events-rule-syntax)
+ [Properties](#w3ab2c21c10d682b9)
+ [Return Value](#w3ab2c21c10d682c11)
+ [Examples](#w3ab2c21c10d682c13)

## Syntax<a name="aws-resource-events-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-rule-syntax.json"></a>

```
{
  "Type" : "AWS::Events::Rule",
  "Properties" : {
    "[Description](#cfn-events-rule-description)" : String,
    "[EventPattern](#cfn-events-rule-eventpattern)" : JSON object,
    "[Name](#cfn-events-rule-name)" : String,
    "[ScheduleExpression](#cfn-events-rule-scheduleexpression)" : String,
    "[State](#cfn-events-rule-state)" : String,
    "[Targets](#cfn-events-rule-targets)" : [ [Target](aws-properties-events-rule-target.md), ... ]
  }
}
```

### YAML<a name="aws-resource-events-rule-syntax.yaml"></a>

```
Type: "AWS::Events::Rule"
Properties: 
  [Description](#cfn-events-rule-description): String
  [EventPattern](#cfn-events-rule-eventpattern): JSON object
  [Name](#cfn-events-rule-name): String
  [ScheduleExpression](#cfn-events-rule-scheduleexpression): String
  [State](#cfn-events-rule-state): String
  [Targets](#cfn-events-rule-targets):
    - [Target](aws-properties-events-rule-target.md)
```

## Properties<a name="w3ab2c21c10d682b9"></a>

`Description`  <a name="cfn-events-rule-description"></a>
A description of the rule's purpose\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EventPattern`  <a name="cfn-events-rule-eventpattern"></a>
Describes which events CloudWatch Events routes to the specified target\. These routed events are matched events\. For more information, see [Events and Event Patterns](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/CloudWatchEventsandEventPatterns.html) in the *Amazon CloudWatch User Guide*\.  
*Required*: Conditional\. You must specify this property, the `ScheduleExpression` property, or both\.  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-events-rule-name"></a>
A name for the rule\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the rule name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ScheduleExpression`  <a name="cfn-events-rule-scheduleexpression"></a>
The schedule or rate \(frequency\) that determines when CloudWatch Events runs the rule\. For more information, see [Schedule Expression Syntax for Rules](http://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html) in the *Amazon CloudWatch User Guide*\.  
*Required*: Conditional\. You must specify this property, the `EventPattern` property, or both\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`State`  <a name="cfn-events-rule-state"></a>
Indicates whether the rule is enabled\. For valid values, see the `State` parameter for the [PutRule](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutRule.html) action in the *Amazon CloudWatch Events API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Targets`  <a name="cfn-events-rule-targets"></a>
The resources, such as Lambda functions or Kinesis streams, that CloudWatch Events routes events to and invokes when the rule is triggered\. For information about valid targets, see the [PutTargets](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_PutTargets.html) action in the *Amazon CloudWatch Events API Reference*\.  
Creating rules with built\-in targets is supported only in the AWS Management Console\.
*Required*: No  
*Type*: List of [Amazon CloudWatch Events Rule Target](aws-properties-events-rule-target.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d682c11"></a>

### Ref<a name="w3ab2c21c10d682c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the event rule ID, such as `mystack-ScheduledRule-ABCDEFGHIJK`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d682c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The event rule Amazon Resource Name \(ARN\), such as `arn:aws:events:``us-east-2``:123456789012:rule/example`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d682c13"></a>

### Regularly Invoke Lambda Function<a name="w3ab2c21c10d682c13b2"></a>

The following example creates a rule that invokes the specified Lambda function every 10 minutes\. The `PermissionForEventsToInvokeLambda` resource grants CloudWatch Events permission to invoke the associated function\.

#### JSON<a name="aws-resource-events-rule-example.json"></a>

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

#### YAML<a name="aws-resource-events-rule-example.yaml"></a>

```
ScheduledRule: 
  Type: "AWS::Events::Rule"
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
  Type: "AWS::Lambda::Permission"
  Properties: 
    FunctionName: 
      Ref: "LambdaFunction"
    Action: "lambda:InvokeFunction"
    Principal: "events.amazonaws.com"
    SourceArn: 
      Fn::GetAtt: 
        - "ScheduledRule"
        - "Arn"
```

### Invoke Lambda Function in Response to an Event<a name="w3ab2c21c10d682c13b4"></a>

The following example creates a rule that invokes the specified Lambda function when any EC2 instance's state changes to `stopping`\.

#### JSON<a name="aws-resource-events-rule-example2.json"></a>

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

#### YAML<a name="aws-resource-events-rule-example2.yaml"></a>

```
EventRule: 
  Type: "AWS::Events::Rule"
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
  Type: "AWS::Lambda::Permission"
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

### Notify a Topic in Response to a Log Entry<a name="w3ab2c21c10d682c13b6"></a>

The following example creates a rule that notifies an Amazon Simple Notification Service topic if an AWS CloudTrail log entry contains a call by the `Root` user\.

#### JSON<a name="aws-resource-events-rule-example3.json"></a>

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
```

#### YAML<a name="aws-resource-events-rule-example3.yaml"></a>

```
OpsEventRule: 
  Type: "AWS::Events::Rule"
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
```