# AWS::SQS::QueuePolicy<a name="aws-properties-sqs-policy"></a>

The `AWS::SQS::QueuePolicy` type applies a policy to Amazon SQS queues\. For an example snippet, see [Declaring an Amazon SQS Policy](AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-sqs-policy) in the *AWS CloudFormation User Guide*\. 

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
Properties : 
﻿  [PolicyDocument](#cfn-sqs-queuepolicy-policydoc) : Json
﻿  [Queues](#cfn-sqs-queuepolicy-queues) : 
    - String
```

## Properties<a name="aws-properties-sqs-policy-properties"></a>

`PolicyDocument`  <a name="cfn-sqs-queuepolicy-policydoc"></a>
A policy document that contains the permissions for the specified Amazon SQS queues\. For more information about Amazon SQS policies, see [Creating Custom Policies Using the Access Policy Language](AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-creating-custom-policies.html) in the *Amazon Simple Queue Service Developer Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queues`  <a name="cfn-sqs-queuepolicy-queues"></a>
The URLs of the queues to which you want to add the policy\. You can use the `[Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)` function to specify an `[AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)