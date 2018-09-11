# Amazon SQS Template Snippets<a name="scenario-sqs-queue"></a>

This example shows an Amazon SQS queue\.

## JSON<a name="scenario-sqs-queue-example-1.json"></a>

```
"MyQueue" : {
    "Type" : "AWS::SQS::Queue",
    "Properties" : {
        "VisibilityTimeout" : "value"
    }
}
```

## YAML<a name="scenario-sqs-queue-example-1.yaml"></a>

```
MyQueue:
  Type: AWS::SQS::Queue
  Properties:
    VisibilityTimeout: value
```