# AWS::SQS::QueuePolicy<a name="aws-properties-sqs-policy"></a>

The `AWS::SQS::QueuePolicy` type applies a policy to Amazon SQS queues\. For an example snippet, see [Declaring an Amazon SQS Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-sqs-policy) in the *AWS CloudFormation User Guide*\. 

## Syntax<a name="aws-properties-sqs-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sqs-policy-syntax.json"></a>

```
{
  "Type" : "AWS::SQS::QueuePolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-sqs-queuepolicy-policydoc)" : Json,
      "[Queues](#cfn-sqs-queuepolicy-queues)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-properties-sqs-policy-syntax.yaml"></a>

```
Type: AWS::SQS::QueuePolicy
Properties: 
  [PolicyDocument](#cfn-sqs-queuepolicy-policydoc): Json
  [Queues](#cfn-sqs-queuepolicy-queues): 
    - String
```

## Properties<a name="aws-properties-sqs-policy-properties"></a>

`PolicyDocument`  <a name="cfn-sqs-queuepolicy-policydoc"></a>
A policy document that contains the permissions for the specified Amazon SQS queues\. For more information about Amazon SQS policies, see [Creating Custom Policies Using the Access Policy Language](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-creating-custom-policies.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queues`  <a name="cfn-sqs-queuepolicy-queues"></a>
The URLs of the queues to which you want to add the policy\. You can use the `[Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)` function to specify an `[AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-sqs-policy--examples"></a>



### Amazon SQS Queue Policy<a name="aws-properties-sqs-policy--examples--Amazon_SQS_Queue_Policy"></a>

The following sample is a queue policy that allows AWS account 111122223333 to send and receive messages on queue queue2\. You add the policy to the resources section of your template\.

#### JSON<a name="aws-properties-sqs-policy--examples--Amazon_SQS_Queue_Policy--json"></a>

```
 
"SampleSQSPolicy" : {
  "Type" : "AWS::SQS::QueuePolicy",
  "Properties" : {
    "Queues" :  ["https://sqs:us-east-2.amazonaws.com/444455556666/queue2"],
    "PolicyDocument": {
      "Statement":[{
        "Action":["SQS:SendMessage", "SQS:ReceiveMessage"],
        "Effect":"Allow",
        "Resource": "arn:aws:sqs:us-east-2:444455556666:queue2",
        "Principal": {
          "AWS": [
            "111122223333"]
        }
      }]
    }
  }
}
```

#### YAML<a name="aws-properties-sqs-policy--examples--Amazon_SQS_Queue_Policy--yaml"></a>

```
 
SampleSQSPolicy: 
  Type: AWS::SQS::QueuePolicy
  Properties: 
    Queues: 
      - "https://sqs:us-east-2.amazonaws.com/444455556666/queue2"
    PolicyDocument: 
      Statement: 
        - 
          Action: 
            - "SQS:SendMessage" 
            - "SQS:ReceiveMessage"
          Effect: "Allow"
          Resource: "arn:aws:sqs:us-east-2:444455556666:queue2"
          Principal:  
            AWS: 
              - "111122223333"
```