# AWS::FraudDetector::Detector<a name="aws-resource-frauddetector-detector"></a>

Manages a detector and associated detector versions\.

## Syntax<a name="aws-resource-frauddetector-detector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-frauddetector-detector-syntax.json"></a>

```
{
  "Type" : "AWS::FraudDetector::Detector",
  "Properties" : {
      "[AssociatedModels](#cfn-frauddetector-detector-associatedmodels)" : [ Model, ... ],
      "[Description](#cfn-frauddetector-detector-description)" : String,
      "[DetectorId](#cfn-frauddetector-detector-detectorid)" : String,
      "[DetectorVersionStatus](#cfn-frauddetector-detector-detectorversionstatus)" : String,
      "[EventType](#cfn-frauddetector-detector-eventtype)" : EventType,
      "[RuleExecutionMode](#cfn-frauddetector-detector-ruleexecutionmode)" : String,
      "[Rules](#cfn-frauddetector-detector-rules)" : [ Rule, ... ],
      "[Tags](#cfn-frauddetector-detector-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-frauddetector-detector-syntax.yaml"></a>

```
Type: AWS::FraudDetector::Detector
Properties: 
  [AssociatedModels](#cfn-frauddetector-detector-associatedmodels): 
    - Model
  [Description](#cfn-frauddetector-detector-description): String
  [DetectorId](#cfn-frauddetector-detector-detectorid): String
  [DetectorVersionStatus](#cfn-frauddetector-detector-detectorversionstatus): String
  [EventType](#cfn-frauddetector-detector-eventtype): 
    EventType
  [RuleExecutionMode](#cfn-frauddetector-detector-ruleexecutionmode): String
  [Rules](#cfn-frauddetector-detector-rules): 
    - Rule
  [Tags](#cfn-frauddetector-detector-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-frauddetector-detector-properties"></a>

`AssociatedModels`  <a name="cfn-frauddetector-detector-associatedmodels"></a>
The models to associate with this detector\. You must provide the ARNs of all the models you want to associate\.   
*Required*: No  
*Type*: List of [Model](aws-properties-frauddetector-detector-model.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-frauddetector-detector-description"></a>
The detector description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetectorId`  <a name="cfn-frauddetector-detector-detectorid"></a>
 The name of the detector\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[0-9a-z_-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DetectorVersionStatus`  <a name="cfn-frauddetector-detector-detectorversionstatus"></a>
The status of the detector version\. If a value is not provided for this property, AWS CloudFormation assumes `DRAFT` status\.  
 Valid values: `ACTIVE | DRAFT`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventType`  <a name="cfn-frauddetector-detector-eventtype"></a>
The event type associated with this detector\.  
*Required*: Yes  
*Type*: [EventType](aws-properties-frauddetector-detector-eventtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleExecutionMode`  <a name="cfn-frauddetector-detector-ruleexecutionmode"></a>
The rule execution mode for the rules included in the detector version\.  
Valid values: `FIRST_MATCHED | ALL_MATCHED` Default value: `FIRST_MATCHED`  
You can define and edit the rule mode at the detector version level, when it is in draft status\.   
If you specify `FIRST_MATCHED`, Amazon Fraud Detector evaluates rules sequentially, first to last, stopping at the first matched rule\. Amazon Fraud dectector then provides the outcomes for that single rule\.  
If you specifiy `ALL_MATCHED`, Amazon Fraud Detector evaluates all rules and returns the outcomes for all matched rules\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-frauddetector-detector-rules"></a>
The rules to include in the detector version\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-frauddetector-detector-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-frauddetector-detector-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-frauddetector-detector-return-values"></a>

### Ref<a name="aws-resource-frauddetector-detector-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the primary identifier for the resource, which is the ARN\.

Example: `{"Ref": "arn:aws:frauddetector:us-west-2:123123123123:outcome/outcome_name"}`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-frauddetector-detector-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-frauddetector-detector-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The detector ARN\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Timestamp of when detector was created\.

`DetectorVersionId`  <a name="DetectorVersionId-fn::getatt"></a>
The name of the detector\.

`EventType.Arn`  <a name="EventType.Arn-fn::getatt"></a>
Property description not available\.

`EventType.CreatedTime`  <a name="EventType.CreatedTime-fn::getatt"></a>
Property description not available\.

`EventType.LastUpdatedTime`  <a name="EventType.LastUpdatedTime-fn::getatt"></a>
Property description not available\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Timestamp of when detector was last updated\.

## See also<a name="aws-resource-frauddetector-detector--seealso"></a>
+ [CreateDetectorVersion](https://docs.aws.amazon.com/frauddetector/latest/api/API_CreateDetectorVersion.html) in the *Amazon Fraud Detector API Reference*\.
+ [Create a detector version](https://docs.aws.amazon.com/frauddetector/latest/ug/create-a-detector-version.html) in the *Amazon Fraud Detector User Guide*\.