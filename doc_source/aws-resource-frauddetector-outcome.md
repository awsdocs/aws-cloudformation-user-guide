# AWS::FraudDetector::Outcome<a name="aws-resource-frauddetector-outcome"></a>

Creates or updates an outcome\. 

## Syntax<a name="aws-resource-frauddetector-outcome-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-frauddetector-outcome-syntax.json"></a>

```
{
  "Type" : "AWS::FraudDetector::Outcome",
  "Properties" : {
      "[Description](#cfn-frauddetector-outcome-description)" : String,
      "[Name](#cfn-frauddetector-outcome-name)" : String,
      "[Tags](#cfn-frauddetector-outcome-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-frauddetector-outcome-syntax.yaml"></a>

```
Type: AWS::FraudDetector::Outcome
Properties: 
  [Description](#cfn-frauddetector-outcome-description): String
  [Name](#cfn-frauddetector-outcome-name): String
  [Tags](#cfn-frauddetector-outcome-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-frauddetector-outcome-properties"></a>

`Description`  <a name="cfn-frauddetector-outcome-description"></a>
The outcome description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-outcome-name"></a>
The outcome name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[0-9a-z_-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-frauddetector-outcome-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-frauddetector-outcome-return-values"></a>

### Ref<a name="aws-resource-frauddetector-outcome-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the primary identifier for the resource, which is the ARN\.

Example: `{"Ref": "arn:aws:frauddetector:us-west-2:123123123123:outcome/outcome_name"}`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-frauddetector-outcome-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-frauddetector-outcome-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the outcome\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Timestamp of when outcome was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Timestamp of when outcome was last updated\.

## See also<a name="aws-resource-frauddetector-outcome--seealso"></a>
+ [PutOutcome](https://docs.aws.amazon.com/frauddetector/latest/api/API_PutOutcome.html) in the *Amazon Fraud Detector API Reference*
+ [Create an outcome](https://docs.aws.amazon.com/frauddetector/latest/ug/create-an-outcome.html) in the *Amazon Fraud Detector User Guide*