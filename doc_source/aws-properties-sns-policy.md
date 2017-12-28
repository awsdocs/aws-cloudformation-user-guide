# AWS::SNS::TopicPolicy<a name="aws-properties-sns-policy"></a>

The `AWS::SNS::TopicPolicy` resource associates Amazon SNS topics with a policy\.


+ [Syntax](#aws-resource-sns-policy-syntax)
+ [Properties](#w3ab2c21c10d990b9)

## Syntax<a name="aws-resource-sns-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sns-policy-syntax.json"></a>

```
{
  "Type" : "AWS::SNS::TopicPolicy",
  "Properties" :
    {
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topicpolicy-policydocument)" : PolicyDocument,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topicpolicy-topics)" : [ List of SNS topic ARNs, ... ]
    }
}
```

### YAML<a name="aws-resource-sns-policy-syntax.yaml"></a>

```
Type: "AWS::SNS::TopicPolicy"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topicpolicy-policydocument): PolicyDocument
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-sns-topicpolicy-topics):
    - List of SNS topic ARNs
```

## Properties<a name="w3ab2c21c10d990b9"></a>

`PolicyDocument`  
A policy document that contains permissions to add to the specified SNS topics\.  
*Required: *Yes  
JSON or YAML  
*Update requires*: No interruption

`Topics`  
The Amazon Resource Names \(ARN\) of the topics to which you want to add the policy\. You can use the Ref function to specify an AWS::SNS::Topic resource\.  
*Required: *Yes  
*Type*: A list of Amazon SNS topics ARNs  
*Update requires*: No interruption

For sample `AWS::SNS::TopicPolicy` snippets, see \.