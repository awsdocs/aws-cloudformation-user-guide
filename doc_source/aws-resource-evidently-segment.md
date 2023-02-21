# AWS::Evidently::Segment<a name="aws-resource-evidently-segment"></a>

Creates or updates a *segment* of your audience\. A segment is a portion of your audience that share one or more characteristics\. Examples could be Chrome browser users, users in Europe, or Firefox browser users in Europe who also fit other criteria that your application collects, such as age\.

Using a segment in an experiment limits that experiment to evaluate only the users who match the segment criteria\. Using one or more segments in a launch allow you to define different traffic splits for the different audience segments\.

For more information about segment pattern syntax, see [ Segment rule pattern syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments-syntax.html)\.

The pattern that you define for a segment is matched against the value of `evaluationContext`, which is passed into Evidently in the [EvaluateFeature](https://docs.aws.amazon.com/cloudwatchevidently/latest/APIReference/API_EvaluateFeature.html) operation, when Evidently assigns a feature variation to a user\.

## Syntax<a name="aws-resource-evidently-segment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-evidently-segment-syntax.json"></a>

```
{
  "Type" : "AWS::Evidently::Segment",
  "Properties" : {
      "[Description](#cfn-evidently-segment-description)" : String,
      "[Name](#cfn-evidently-segment-name)" : String,
      "[Pattern](#cfn-evidently-segment-pattern)" : String,
      "[Tags](#cfn-evidently-segment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-evidently-segment-syntax.yaml"></a>

```
Type: AWS::Evidently::Segment
Properties: 
  [Description](#cfn-evidently-segment-description): String
  [Name](#cfn-evidently-segment-name): String
  [Pattern](#cfn-evidently-segment-pattern): String
  [Tags](#cfn-evidently-segment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-evidently-segment-properties"></a>

`Description`  <a name="cfn-evidently-segment-description"></a>
An optional description for this segment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-evidently-segment-name"></a>
A name for the segment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pattern`  <a name="cfn-evidently-segment-pattern"></a>
The pattern to use for the segment\. For more information about pattern syntax, see [ Segment rule pattern syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments-syntax.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-evidently-segment-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the feature\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with a feature\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-evidently-segment-return-values"></a>

### Ref<a name="aws-resource-evidently-segment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the segment\. For example, `arn:aws:evidently:us-west-2:123456789012:segment/australiaSegment`

### Fn::GetAtt<a name="aws-resource-evidently-segment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-evidently-segment-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the segment\. For example, `arn:aws:evidently:us-west-2:123456789012:segment/australiaSegment`