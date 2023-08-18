# AWS::SNS::TopicInlinePolicy<a name="aws-resource-sns-topicinlinepolicy"></a>

The `AWS::SNS::TopicInlinePolicy` resource associates one Amazon SNS topic with one policy\.

## Syntax<a name="aws-resource-sns-topicinlinepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sns-topicinlinepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::TopicInlinePolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-sns-topicinlinepolicy-policydocument)" : Json,
      "[TopicArn](#cfn-sns-topicinlinepolicy-topicarn)" : String
    }
}
```

### YAML<a name="aws-resource-sns-topicinlinepolicy-syntax.yaml"></a>

```
Type: AWS::SNS::TopicInlinePolicy
Properties: 
  [PolicyDocument](#cfn-sns-topicinlinepolicy-policydocument): Json
  [TopicArn](#cfn-sns-topicinlinepolicy-topicarn): String
```

## Properties<a name="aws-resource-sns-topicinlinepolicy-properties"></a>

`PolicyDocument`  <a name="cfn-sns-topicinlinepolicy-policydocument"></a>
A policy document that contains permissions to add to the specified Amazon SNS topic\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-sns-topicinlinepolicy-topicarn"></a>
The Amazon Resource Name \(ARN\) of the topic to which you want to add the policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sns-topicinlinepolicy-return-values"></a>

### Ref<a name="aws-resource-sns-topicinlinepolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the topic for which the policy was added\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.