# AWS::FraudDetector::Label<a name="aws-resource-frauddetector-label"></a>

Creates or updates label\. A label classifies an event as fraudulent or legitimate\. Labels are associated with event types and used to train supervised machine learning models in Amazon Fraud Detector\. 

## Syntax<a name="aws-resource-frauddetector-label-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-frauddetector-label-syntax.json"></a>

```
{
  "Type" : "AWS::FraudDetector::Label",
  "Properties" : {
      "[Description](#cfn-frauddetector-label-description)" : String,
      "[Name](#cfn-frauddetector-label-name)" : String,
      "[Tags](#cfn-frauddetector-label-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-frauddetector-label-syntax.yaml"></a>

```
Type: AWS::FraudDetector::Label
Properties: 
  [Description](#cfn-frauddetector-label-description): String
  [Name](#cfn-frauddetector-label-name): String
  [Tags](#cfn-frauddetector-label-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-frauddetector-label-properties"></a>

`Description`  <a name="cfn-frauddetector-label-description"></a>
The label description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-label-name"></a>
The label name\.  
Pattern: `^[0-9a-z_-]+$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-frauddetector-label-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-frauddetector-label-return-values"></a>

### Ref<a name="aws-resource-frauddetector-label-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the primary identifier for the resource, which is the ARN\.

Example: `{"Ref": "arn:aws:frauddetector:us-west-2:123123123123:outcome/outcome_name"}`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-frauddetector-label-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-frauddetector-label-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the label\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Timestamp of when label was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Timestamp of when label was last updated\.

## See also<a name="aws-resource-frauddetector-label--seealso"></a>
+ [PutLabel](https://docs.aws.amazon.com/frauddetector/latest/api/API_PutLabel.html) in the *Amazon Fraud Detector API Reference*
+ [Create a label](https://docs.aws.amazon.com/frauddetector/latest/ug/create-a-label.html) in the *Amazon Fraud Detector User Guide*