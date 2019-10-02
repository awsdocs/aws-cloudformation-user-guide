# AWS::GuardDuty::Filter<a name="aws-resource-guardduty-filter"></a>

The `AWS::GuardDuty::Filter` resource specifies a new filter defined by the provided `findingCriteria`\.

## Syntax<a name="aws-resource-guardduty-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-filter-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::Filter",
  "Properties" : {
      "[Action](#cfn-guardduty-filter-action)" : String,
      "[Description](#cfn-guardduty-filter-description)" : String,
      "[DetectorId](#cfn-guardduty-filter-detectorid)" : String,
      "[FindingCriteria](#cfn-guardduty-filter-findingcriteria)" : [FindingCriteria](aws-properties-guardduty-filter-findingcriteria.md),
      "[Name](#cfn-guardduty-filter-name)" : String,
      "[Rank](#cfn-guardduty-filter-rank)" : Integer
    }
}
```

### YAML<a name="aws-resource-guardduty-filter-syntax.yaml"></a>

```
Type: AWS::GuardDuty::Filter
Properties: 
  [Action](#cfn-guardduty-filter-action): String
  [Description](#cfn-guardduty-filter-description): String
  [DetectorId](#cfn-guardduty-filter-detectorid): String
  [FindingCriteria](#cfn-guardduty-filter-findingcriteria): 
    [FindingCriteria](aws-properties-guardduty-filter-findingcriteria.md)
  [Name](#cfn-guardduty-filter-name): String
  [Rank](#cfn-guardduty-filter-rank): Integer
```

## Properties<a name="aws-resource-guardduty-filter-properties"></a>

`Action`  <a name="cfn-guardduty-filter-action"></a>
Specifies the action that is to be applied to the findings that match the filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-guardduty-filter-description"></a>
The description of the filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DetectorId`  <a name="cfn-guardduty-filter-detectorid"></a>
The ID of the detector to associate the `Filter` with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FindingCriteria`  <a name="cfn-guardduty-filter-findingcriteria"></a>
Represents the criteria to be used in the filter for querying findings\.  
*Required*: Yes  
*Type*: [FindingCriteria](aws-properties-guardduty-filter-findingcriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-guardduty-filter-name"></a>
The name of the filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rank`  <a name="cfn-guardduty-filter-rank"></a>
Specifies the position of the filter in the list of current filters\. Also specifies the order in which this filter is applied to the findings\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-guardduty-filter-return-values"></a>

### Ref<a name="aws-resource-guardduty-filter-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the filter, such as `SampleFilter`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-guardduty-filter--examples"></a>

### Declare a Filter Resource<a name="aws-resource-guardduty-filter--examples--Declare_a_Filter_Resource"></a>

The following example shows how to declare a GuardDuty `Filter` resource:

#### JSON<a name="aws-resource-guardduty-filter--examples--Declare_a_Filter_Resource--json"></a>

```
{
    "Type": "AWS::GuardDuty::Filter",
    "Properties": {
        "Action": "ARCHIVE",
        "Description": "SampleFilter",
        "DetectorId": "a12abc34d567e8fa901bc2d34e56789f0",
        "FindingCriteria": {
            "Criterion": {
                "updatedAt": {
                "Gte": 0
                }
        }
    },
    "Rank": 1,
    "Name": "SampleFilter"
    }
}
```

#### YAML<a name="aws-resource-guardduty-filter--examples--Declare_a_Filter_Resource--yaml"></a>

```
Type: "AWS::GuardDuty::Filter"
Properties:
    Action : "ARCHIVE"
    Description : "SampleFilter"
    DetectorId : "a12abc34d567e8fa901bc2d34e56789f0"
    FindingCriteria : 
        Criterion:
            "updatedAt":
                Gte: 0	
    Rank : 1
    Name : "SampleFilter"
```

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
