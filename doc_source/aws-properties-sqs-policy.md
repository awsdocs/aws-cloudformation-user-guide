# AWS::SQS::QueuePolicy<a name="aws-properties-sqs-policy"></a>

The AWS::SQS::QueuePolicy type applies a policy to Amazon SQS queues\.

AWS::SQS::QueuePolicy Snippet: [Declaring an Amazon SQS Policy](quickref-iam.md#scenario-sqs-policy)

**Topics**
+ [Syntax](#aws-resource-sqs-queuepolicy-syntax)
+ [Properties](#w3ab2c21c10e1144c11)

## Syntax<a name="aws-resource-sqs-queuepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sqs-queuepolicy-syntax.json"></a>

```
{
   "Type" : "AWS::SQS::QueuePolicy",
   "Properties" : {
      "[PolicyDocument](#cfn-sqs-queuepolicy-policydoc)" : JSON,
      "[Queues](#cfn-sqs-queuepolicy-queues)" : [ String, ... ]
   }
}
```

### YAML<a name="aws-resource-sqs-queuepolicy-syntax.yaml"></a>

```
Type: "AWS::SQS::QueuePolicy"
Properties: 
  [PolicyDocument](#cfn-sqs-queuepolicy-policydoc): JSON
  [Queues](#cfn-sqs-queuepolicy-queues):
    - String
```

## Properties<a name="w3ab2c21c10e1144c11"></a>

`PolicyDocument`  <a name="cfn-sqs-queuepolicy-policydoc"></a>
A policy document that contains the permissions for the specified Amazon SQS queues\. For more information about Amazon SQS policies, see [Creating Custom Policies Using the Access Policy Language](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-creating-custom-policies.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Queues`  <a name="cfn-sqs-queuepolicy-queues"></a>
The URLs of the queues to which you want to add the policy\. You can use the [Ref function](intrinsic-function-reference-ref.md) to specify an [AWS::SQS::Queue](aws-properties-sqs-queues.md) resource\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)