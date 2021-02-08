# Amazon SQS template snippets<a name="scenario-sqs-queue"></a>

This example shows an Amazon SQS queue\.

## JSON<a name="scenario-sqs-queue-example-1.json"></a>

```
1. "MyQueue" : {
2.     "Type" : "AWS::SQS::Queue",
3.     "Properties" : {
4.         "VisibilityTimeout" : "value"
5.     }
6. }
```

## YAML<a name="scenario-sqs-queue-example-1.yaml"></a>

```
1. MyQueue:
2.   Type: AWS::SQS::Queue
3.   Properties:
4.     VisibilityTimeout: value
```