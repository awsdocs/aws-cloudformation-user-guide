# AWS::GuardDuty::Detector<a name="aws-resource-guardduty-detector"></a>

The `AWS::GuardDuty::Detector` resource specifies a new Amazon GuardDuty detector\. A detector is an object that represents the Amazon GuardDuty service\. A detector is required for Amazon GuardDuty to become operational\.

## Syntax<a name="aws-resource-guardduty-detector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-detector-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Detector",
  "Properties" : {
      "[Enable](#cfn-guardduty-detector-enable)" : Boolean,
      "[FindingPublishingFrequency](#cfn-guardduty-detector-findingpublishingfrequency)" : String
    }
}
```

### YAML<a name="aws-resource-guardduty-detector-syntax.yaml"></a>

```
Type: AWS::GuardDuty::Detector
Properties: 
  [Enable](#cfn-guardduty-detector-enable): Boolean
  [FindingPublishingFrequency](#cfn-guardduty-detector-findingpublishingfrequency): String
```

## Properties<a name="aws-resource-guardduty-detector-properties"></a>

`Enable`  <a name="cfn-guardduty-detector-enable"></a>
Specifies whether or not to enable the detector\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingPublishingFrequency`  <a name="cfn-guardduty-detector-findingpublishingfrequency"></a>
A enumeration value that specifies how frequently finding updates are published\. Valid values include: FIFTEEN\_MINUTES \| ONE\_HOUR \| SIX\_HOURS\. The default value is SIX\_HOURS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-guardduty-detector-return-values"></a>

### Ref<a name="aws-resource-guardduty-detector-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique ID of the detector\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-guardduty-detector--examples"></a>

### Declare a Detector Resource<a name="aws-resource-guardduty-detector--examples--Declare_a_Detector_Resource"></a>

The following example shows how to declare a GuardDuty `Detector` resource:

#### JSON<a name="aws-resource-guardduty-detector--examples--Declare_a_Detector_Resource--json"></a>

```
"mydetector": {
    "Type" : "AWS::GuardDuty::Detector",
    "Properties" : {
        "Enable" : True,
        "FindingPublishingFrequency" : "FIFTEEN_MINUTES"
    }
}
```

#### YAML<a name="aws-resource-guardduty-detector--examples--Declare_a_Detector_Resource--yaml"></a>

```
mydetector:
    Type: AWS::GuardDuty::Detector
    Properties:
        Enable: True
        FindingPublishingFrequency: FIFTEEN_MINUTES
```