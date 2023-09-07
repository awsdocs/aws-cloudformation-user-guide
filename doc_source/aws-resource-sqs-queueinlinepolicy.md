# AWS::SQS::QueueInlinePolicy<a name="aws-resource-sqs-queueinlinepolicy"></a>

 The `AWS::SQS::QueueInlinePolicy` resource associates one Amazon SQS queue with one policy\. 

## Syntax<a name="aws-resource-sqs-queueinlinepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sqs-queueinlinepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SQS::QueueInlinePolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-sqs-queueinlinepolicy-policydocument)" : Json,
      "[Queue](#cfn-sqs-queueinlinepolicy-queue)" : String
    }
}
```

### YAML<a name="aws-resource-sqs-queueinlinepolicy-syntax.yaml"></a>

```
Type: AWS::SQS::QueueInlinePolicy
Properties: 
  [PolicyDocument](#cfn-sqs-queueinlinepolicy-policydocument): Json
  [Queue](#cfn-sqs-queueinlinepolicy-queue): String
```

## Properties<a name="aws-resource-sqs-queueinlinepolicy-properties"></a>

`PolicyDocument`  <a name="cfn-sqs-queueinlinepolicy-policydocument"></a>
 A policy document that contains the permissions for the specified Amazon SQS queues\. For more information about Amazon SQS policies, see [Using custom policies with the Amazon SQS access policy language](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-creating-custom-policies.html) in the *Amazon SQS Developer Guide*\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queue`  <a name="cfn-sqs-queueinlinepolicy-queue"></a>
The URLs of the queues to which you want to add the policy\. You can use the `[ Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)` function to specify an `[ AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)` resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sqs-queueinlinepolicy-return-values"></a>

### Ref<a name="aws-resource-sqs-queueinlinepolicy-return-values-ref"></a>