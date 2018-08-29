# AWS::GuardDuty::Filter<a name="aws-resource-guardduty-filter"></a>

You can use the `AWS::GuardDuty::Filter` resource to create a GuardDuty filter using the specified finding criteria\. 

**Topics**
+ [Syntax](#aws-resource-guardduty-filter-syntax)
+ [Properties](#aws-resource-guardduty-filter-properties)
+ [Return Values](#aws-resource-guardduty-filter-returnvalues)
+ [Examples](#aws-resource-guardduty-filter-examples)

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
    "[FindingCriteria](#cfn-guardduty-filter-findingcriteria)" : [*FindingCriteria*](aws-properties-guardduty-filter-findingcriteria.md),
    "[Rank](#cfn-guardduty-filter-rank)" : Integer,
    "[Name](#cfn-guardduty-filter-name)" : String
  }
}
```

### YAML<a name="aws-resource-guardduty-filter-syntax.yaml"></a>

```
Type: "AWS::GuardDuty::Filter"
Properties:
  [Action](#cfn-guardduty-filter-action): String
  [Description](#cfn-guardduty-filter-description): String
  [DetectorId](#cfn-guardduty-filter-detectorid): String
  [FindingCriteria](#cfn-guardduty-filter-findingcriteria): [*FindingCriteria*](aws-properties-guardduty-filter-findingcriteria.md)
  [Rank](#cfn-guardduty-filter-rank): Integer
  [Name](#cfn-guardduty-filter-name): String
```

## Properties<a name="aws-resource-guardduty-filter-properties"></a>

`Action`  <a name="cfn-guardduty-filter-action"></a>
Specifies the action that is to be applied to the findings that match the filter\. Valid values are: NOOP \| ARCHIVE  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-guardduty-filter-description"></a>
The description of the filter\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DetectorId`  <a name="cfn-guardduty-filter-detectorid"></a>
The ID of the detector that specifies the GuardDuty service whose findings you want to filter\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FindingCriteria`  <a name="cfn-guardduty-filter-findingcriteria"></a>
Represents the criteria to be used in the filter for querying findings\.  
 *Required*: Yes  
 *Type*: [GuardDuty Filter FindingCriteria](aws-properties-guardduty-filter-findingcriteria.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Rank`  <a name="cfn-guardduty-filter-rank"></a>
Specifies the position of the filter in the list of current filters\. Also specifies the order in which this filter is applied to the findings\.   
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-guardduty-filter-name"></a>
The name of the filter\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-guardduty-filter-returnvalues"></a>

### Ref<a name="aws-resource-guardduty-filter-ref"></a>

When you pass the logical ID of an `AWS::GuardDuty::Filter` resource to the intrinsic `Ref` function, the function returns the name of the created filter, such as `SampleFilter`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-guardduty-filter-examples"></a>

### Declaring a GuardDuty Member Resource<a name="aws-resource-guardduty-filter-example1"></a>

The following example shows how to declare an AWS::GuardDuty::Filter resource to create a filter for your GuardDuty findings\.

#### JSON<a name="aws-resource-guardduty-filter-example1.json"></a>

```
{
  "Type": "AWS::GuardDuty::Filter",
  "Properties": {
    "Action": "Archive",
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

#### YAML<a name="aws-resource-guardduty-filter-example1.yaml"></a>

```
Type: "AWS::GuardDuty::Filter"
Properties:
 Action : "Archive"
 Description : "SampleFilter"
 DetectorId : "a12abc34d567e8fa901bc2d34e56789f0"
 FindingCriteria : 
   Criterion:
      "updatedAt":
          Gte: 0	
 Rank : 1
 Name : "SampleFilter"
```