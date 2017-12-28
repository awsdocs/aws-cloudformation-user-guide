# AWS::SQS::QueuePolicy<a name="aws-properties-sqs-policy"></a>

The AWS::SQS::QueuePolicy type applies a policy to Amazon SQS queues\.

AWS::SQS::QueuePolicy Snippet: 


+ [Syntax](#aws-resource-sqs-queuepolicy-syntax)
+ [Properties](#w3ab2c21c10e1001c11)

## Syntax<a name="aws-resource-sqs-queuepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sqs-queuepolicy-syntax.json"></a>

```
{
   "Type" : "AWS::SQS::QueuePolicy",
   "Properties" : {
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sqs-queuepolicy-policydoc)" : JSON,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sqs-queuepolicy-queues)" : [ String, ... ]
   }
}
```

### YAML<a name="aws-resource-sqs-queuepolicy-syntax.yaml"></a>

```
Type: "AWS::SQS::QueuePolicy"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-sqs-queuepolicy-policydoc): JSON
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-sqs-queuepolicy-queues):
    - String
```

## Properties<a name="w3ab2c21c10e1001c11"></a>

`PolicyDocument`  
A policy document that contains the permissions for the specified Amazon SQS queues\. For more information about Amazon SQS policies, see [Creating Custom Policies Using the Access Policy Language](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-creating-custom-policies.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required: *Yes  
*Type*: JSON object  
*Update requires*: No interruption

`Queues`  
The URLs of the queues to which you want to add the policy\. You can use the Ref function to specify an AWS::SQS::Queue resource\.  
*Required: *Yes  
*Type*: List of String values  
*Update requires*: No interruption