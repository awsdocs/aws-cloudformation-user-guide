# AWS::SNS::TopicPolicy<a name="aws-resource-sns-topicpolicy"></a>

The `AWS::SNS::TopicPolicy` resource associates Amazon SNS topics with a policy\. For an example snippet, see [Declaring an Amazon SNS policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-sns-policy) in the *AWS CloudFormation User Guide*\.

## Syntax<a name="aws-resource-sns-topicpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sns-topicpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::TopicPolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-sns-topicpolicy-policydocument)" : Json,
      "[Topics](#cfn-sns-topicpolicy-topics)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-sns-topicpolicy-syntax.yaml"></a>

```
Type: AWS::SNS::TopicPolicy
Properties: 
  [PolicyDocument](#cfn-sns-topicpolicy-policydocument): Json
  [Topics](#cfn-sns-topicpolicy-topics): 
    - String
```

## Properties<a name="aws-resource-sns-topicpolicy-properties"></a>

`PolicyDocument`  <a name="cfn-sns-topicpolicy-policydocument"></a>
A policy document that contains permissions to add to the specified SNS topics\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topics`  <a name="cfn-sns-topicpolicy-topics"></a>
The Amazon Resource Names \(ARN\) of the topics to which you want to add the policy\. You can use the ` [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) ` function to specify an ` [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-topic.html) ` resource\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sns-topicpolicy-return-values"></a>

### Fn::GetAtt<a name="aws-resource-sns-topicpolicy-return-values-fn--getatt"></a>

#### <a name="aws-resource-sns-topicpolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The provider\-assigned unique ID for this managed resource\.