# Event type message structure<a name="eventbridge-events"></a>

The notification message that AWS CloudFormation sends to publish an event is in JSON format\. When AWS CloudFormation sends an event to Amazon EventBridge, the following fields are present\. For more information about EventBridge structure, see [Amazon EventBridge events](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-events.html)\.

## Resource status event schema<a name="schema-resource-status-event"></a>

The following schema is the structure for a resource status event\.

```
{
  "version": "0",
  "id": "string",
  "detail-type": "CloudFormation Resource Status Change",
  "source": "string",
  "account": "string",
  "time": "string",
  "region": "string",
  "resources": ["string"],
  "detail": {
    "stack-id" : "string",
    "logical-resource-id" : "string",
    "physical-resource-id": "string",
    "status-details": {
        "status": "string",
        "status-reason": "string"
    },
     "resource-type": "string",
     "client-request-token": "string"
  }
}
```

The following definitions relate to the structure of the status events\.

`version`  
By default, this is set to 0 \(zero\) in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp that can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources that are involved in the event\. The service generating the event determines whether to include these ARNs\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-id`  
The unique stack ID that's associated with the stack\.  
`logical-resource-id`  
The logical name of the resource as specified in the template\.  
`physical-resource-id`  
The name or unique identifier that corresponds to a physical instance ID of a resource supported by CloudFormation\.  
`status-details`    
`status`  
Status of the resource\.  
`status-reason`  
Status reason of the resource\.

`resource-type`  
Type of resource\. For example, `AWS::S3::Bucket`\.

`client-request-token`  
An access token used to call the API\. All events that are initiated by a given stack operation are assigned the same client request token, which you can use to track operations\. Stack operations that are initiated from the console use the token format *Console\-StackOperation\-ID*, which helps you to easily identify the stack operation\. For example, if you create a stack using the console, each resulting stack event would be assigned the same token in the following format: `Console-CreateStack-7f59c3cf-00d2-40c7-b2ff-e75db0987002`\.

**Example Resource status event**  <a name="schema-resource-status-event.example"></a>
The following is an example response for the resource status event\.  

```
{
    "version":"0",
    "id":"6a7e8feb-b491-4cf7-a9f1-bf3703467718",
    "detail-type":"CloudFormation Resource Status Change",
    "source":"aws.cloudformation",
    "account":"111122223333",
    "time":"2017-12-22T18:43:48Z",
    "region":"us-west-1",
    "resources":[
        "arn:aws:cloudformation:us-west-1:111122223333:stack/teststack"
    ],
    "detail":{
        "stack-id":"arn:aws:cloudformation:us-west-1:111122223333:stack/teststack",
        "logical-resource-id":"my-s3-bucket",
        "physical-resource-id":"arn:aws:s3:::my-s3-bucket-us-east-1",
        "status-details":{
            "status":"CREATE_COMPLETE",
            "status-reason":""
        },
        "resource-type":"AWS::S3::Bucket",
        "client-request-token":""
    }
}
```

## Stack status event schema<a name="schema-stack-status-event"></a>

The following schema is the structure for a stack status event\.

```
{
    "version":"0",
    "id":"string",
    "detail-type":"CloudFormation Stack Status Change",
    "source":"string",
    "account":"string",
    "time":"string",
    "region":"string",
    "resources": ["string"],
    "detail":{
        "stack-id":"string",
        "status-details":{
            "status":"string",
            "status-reason":"string"
        },
        "client-request-token":"string"
    }
}
```

The following definitions relates to the structure of the stack status events\.

`version`  
By default, this is set to 0 in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp that can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources that are involved in the event\. The service generating the event determines whether to include these ARNs\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-id`  
The unique stack ID that's associated with the stack\.  
`status-details`    
`status`  
Status of the resource\.  
`status-reason`  
Status reason of the resource\.

`client-request-token`  
An access token used to call the API\. All events that are initiated by a given stack operation are assigned the same client request token, which you can use to track operations\. Stack operations that are initiated from the console use the token format *Console\-StackOperation\-ID*, which helps you to easily identify the stack operation\. For example, if you create a stack using the console, each resulting stack event would be assigned the same token in the following format: `Console-CreateStack-7f59c3cf-00d2-40c7-b2ff-e75db0987002`\.

**Example Stack status event schema**  <a name="schema-stack-status-event.example"></a>
The following is an example response for a stack status event schema\.  

```
{
    "version":"0",
    "id":"6a7e8feb-b491-4cf7-a9f1-bf3703467718",
    "detail-type":"CloudFormation Stack Status Change",
    "source":"aws.cloudformation",
    "account":"111122223333",
    "time":"2017-12-22T18:43:48Z",
    "region":"us-west-1",
    "resources":[
        "arn:aws:cloudformation:us-west-1:111122223333:stack/teststack"
    ],
    "detail":{
        "stack-id":"arn:aws:cloudformation:us-west-1:111122223333:stack/teststack",
        "status-details":{
            "status":"CREATE_COMPLETE",
            "status-reason":""
        },
        "client-request-token":""
    }
}
```

## Stack drift detection event schema<a name="schema-stack-drift-detection"></a>

The following schema is the structure for a stack drift detection event\.

```
{
    "version":"0",
    "id":"string",
    "detail-type":"CloudFormation Drift Detection Status Change",
    "source":"string",
    "account":"string",
    "time":"string",
    "region":"string",
    "resources": ["string"],
    "detail":{
        "stack-id":"string",
        "stack-drift-detection-id":"string",
        "status-details":{
            "stack-drift-status":"string",
            "detection-status":"string"
        },
        "drift-detection-details":{
            "drifted-stack-resource-count":integer
        },
    "client-request-token":"string"
    }
}
```

The following definitions relate to the structure of the drift detection event\.

`version`  
By default, this is set to 0 in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp that can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources involved in the event\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-id`  
The unique stack ID that's associated with the stack\.  
`stack-drift-detection-id`  
The stack drift detection Id\.  
`status-details`    
`stack-drift-status`  
Drift status of the stack\.  
`detection-status`  
Status of drift detection operation\.  
`drift-detection-details`    
`drifted-stack-resource-count`  
Number of resources drifted\. When the value is `-1`, the drift detection is in progress\. All other non\-\-negative integers represent the actual number of drifted resources\.

`client-request-token`  
An access token used to call the API\. All events that are initiated by a given stack operation are assigned the same client request token, which you can use to track operations\. Stack operations that are initiated from the console use the token format *Console\-StackOperation\-ID*, which helps you to easily identify the stack operation\. For example, if you create a stack using the console, each resulting stack event would be assigned the same token in the following format: `Console-CreateStack-7f59c3cf-00d2-40c7-b2ff-e75db0987002`\.

**Example Stack drift detection event**  <a name="schema-stack-drift-detection.example"></a>
The following is an example response for stack drift detection event\.  

```
{
    "version":"0",
    "id":"6a7e8feb-b491-4cf7-a9f1-bf3703467718",
    "detail-type":"CloudFormation Drift Detection Status Change",
    "source":"aws.cloudformation",
    "account":"111122223333",
    "time":"2017-12-22T18:43:48Z",
    "region":"us-west-1",
    "resources": ["string"],
    "detail":{
        "stack-id":"arn:aws:cloudformation:us-west-1:111122223333:stack/teststack",
        "stack-drift-detection-id":"624af370-311a-11e8-b6b7-500cexample",
        "status-details":{
            "stack-drift-status":"DRIFTED",
            "detection-status":"DETECTION_COMPLETE"
        },
        "drift-detection-details":{
            "drifted-stack-resource-count":1
        },
    "client-request-token":""
    }
}
```

## StackSet status event schema<a name="schema-stackset-status"></a>

The following schema is the structure for a StackSet status event\.

```
{
  "version": "0",
  "id": "string",
  "detail-type": "CloudFormation StackSet Status Change",
  "source": "string",
  "account": "string",
  "time": "string",
  "region": "string",
  "resources": ["string"],
  "detail": {
    "stack-set-arn" : "string",
    "status-details": {
        "status":"string"
    }
  }
}
```

The following definitions relate to the structure of the StackSet status event\.

`version`  
By default, this is set to 0 in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp that can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources involved in the event\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-set-arn`  
The Amazon Resource Name \(ARN\) associated with the StackSet\.  
`status-details`    
`status`  
The StackSet status, which can be `ACTIVE` or `DELETED`\. 

**Example StackSet status event**  <a name="schema-stackset-status.example"></a>
The following is an example response for StackSet status event\.  

```
{
  "version": "0",
  "id": "42h6hb90-hg0w-11op-b01v-0xhnh0934z09",
  "detail-type": "CloudFormation StackSet Status Change",
  "source": "aws.cloudformation",
  "account": "111122223333",
  "time": "2021-09-23T17:06:18Z",
  "region": "us-east-1",
  "resources": [
    "arn:aws:cloudformation:us-east-1:111122223333:stackset/test12345:3f3a3fbe-c937-4eb3-a87d-e36a0af3f663"
  ],
  "detail": {
    "stack-set-arn" : "arn:aws:cloudformation:us-east-1:111122223333:stackset/test12345:3f3a3fbe-c937-4eb3-a87d-e36a0af3f663",
    "status-details": {
        "status":"DELETED"
    }
  }
}
```

## StackSet stack instance status event schema<a name="schema-stackset-stack-instance-status"></a>

The following schema is the structure for a StackSet stack instance status event\.

```
{
  "version": "0",
  "id": "string",
  "detail-type": "CloudFormation StackSet StackInstance Status Change",
  "source": "string",
  "account": "string",
  "time": "string",
  "region": "string",
  "resources": ["string"],
  "detail": {
    "stack-set-arn" : "string",
    "stack-id" : "string",
    "status-details": {
        "status": "string"
        "status-reason": "string"
        "detaild-status": "string"
      }
    }
  }
}
```

The following definitions relate to the structure of the StackSet stack instance status event\.

`version`  
By default, this is set to 0 in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp\. This can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources involved in the event\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-set-arn`  
The Amazon Resource Name \(ARN\) associated with the StackSet\.  
`stack-id`  
The unique stack ID that's associated with the stack instance\.  
`status-details`    
`status`  
The StackSet instance status\. StackSet instance statuses can be `CURRENT`, `OUTDATED`, and `INOPERABLE`\.  
`status-reason`  
Status reason of the StackSet instance\.  
`detailed-status`  
The detailed StackSet instance detailed status\. StackSet instance detailed statuses can be `CANCELLED`, `FAILED`, `INOPERABLE`, `PENDING`, `RUNNING`, or `SUCCEEDED`\.

**Example StackSet stack instance status event**  <a name="schema-stackset-stack-instance-status.example"></a>
The following is an example response for StackSet stack instance status event\.  

```
{
  "version": "0",
  "id": "42h6hb90-hg0w-11op-b01v-0xhnh0934z09",
  "detail-type": "CloudFormation StackSet StackInstance Status Change",
  "source": "aws.cloudformation",
  "account": "111122223333",
  "time": "2021-09-22T19:19:23Z",
  "region": "us-east-1",
  "resources": [
    "arn:aws:cloudformation:us-east-1:111122223333:stackset/test1234:e5f54eea-d041-44ad-94f8-b8268aca1e59"
  ],
  "detail": {
     "stack-set-arn": "arn:aws:cloudformation:us-east-1:111122223333:stackset/test1234:e5f54eea-d041-44ad-94f8-b8268aca1e59",
    "stack-id": "arn:aws:cloudformation:us-west-1:111122223333:stack/teststack",
    "status-details": {
        "status": "OUTDATED",
        "status-reason": "User Initiated",
        "detailed-status": "PENDING"
    }
  }
}
```

## StackSet operation status event schema<a name="schema-stackset-operation-status"></a>

The following schema is the structure for a StackSet operation status event\.

```
{
  "version": "0",
  "id": "string",
  "detail-type": "CloudFormation StackSet Operation Status Change",
  "source": "string",
  "account": "string",
  "time": "string",
  "region": "string",
  "resources": ["string"],
  "detail": {
    "stack-set-arn" : "string",
    "stack-set-operation-id" : "string",
    "status-details": {
        "status": "string"
      }
    }
  }
}
```

The following definitions relate to the structure of the StackSet operation status event\.

`version`  
By default, this is set to 0 in all events\.

`id`  
A unique value generated for every event\. Use the `id` attribute to trace events as they move through rules to targets\.

`detail-type`  
Identifies the fields and values that appear in the detail field\.

`source`  
Identifies the service that generated the event\. This is set to `aws.cloudformation`\.

`account`  
The 12\-digit number identifying an AWS account\.

`time`  
The event timestamp that can be specified by the service originating the event\. If the event spans a time interval, the service can report the start time, so this value might be before the time the event is received\.

`region`  
Identifies the AWS Region where the event originated\.

`resources`  
A JSON array that contains the Amazon Resource Names \(ARNs\) that identify resources involved in the event\.

`detail`  
A JSON object that contains information about the event\. The service generating the event determines the content of this field\.    
`stack-set-arn`  
The Amazon Resource Name \(ARN\) associated with the StackSet\.  
`stack-set-operation-id`  
The unique ID that's associated with the StackSet operation\.  
`status-details`    
`status`  
The StackSet operation status\. StackSet operation statuses can be `RUNNING`, `SUCCEEDED`, `FAILED`, `STOPPING`, `STOPPED`, or `QUEUED`\.

**Example StackSet operation status event**  <a name="schema-stackset-stack-instance-status.example"></a>
The following is an example response for StackSet operation status event\.  

```
{
  "version": "0",
  "id": "4de89905-fd92-6a6b-9509-23c04bcb6a21",
  "detail-type": "CloudFormation StackSet Operation Status Change",
  "source": "aws.cloudformation",
  "account": "111122223333",
  "time": "2021-09-22T05:46:24Z",
  "region": "us-east-1",
  "resources": [
    "arn:aws:cloudformation:us-east-1:111122223333:stackset/test1234:e5f54eea-d041-44ad-94f8-b8268aca1e59"
  ],
  "detail": {
    "stack-set-arn": "arn:aws:cloudformation:us-east-1:111122223333:stackset/test1234:e5f54eea-d041-44ad-94f8-b8268aca1e59",
    "stack-set-operation-id": "ce69adce-2221-4483-8c4b-c51f284f25e8",
    "status-details": {
        "status": "SUCCEEDED"
    }
  }
}
```