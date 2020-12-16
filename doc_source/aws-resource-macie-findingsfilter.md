# AWS::Macie::FindingsFilter<a name="aws-resource-macie-findingsfilter"></a>

The `AWS::Macie::FindingsFilter` resource represents an individual findings filter that you create and save to view, analyze, and manage findings\. A *findings filter* is a set of criteria that specifies which findings to include in the results of a query for findings\. A findings filter can also perform specific actions on findings that meet the filter's criteria\.

A `Session` must exist for the account before you can create a `FindingsFilter`\. Use a [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to ensure that the `Session` is created before the other resources\. For example, `"DependsOn: Session"`\.

## Syntax<a name="aws-resource-macie-findingsfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-macie-findingsfilter-syntax.json"></a>

```
{
  "Type" : "AWS::Macie::FindingsFilter",
  "Properties" : {
      "[Action](#cfn-macie-findingsfilter-action)" : String,
      "[Description](#cfn-macie-findingsfilter-description)" : String,
      "[FindingCriteria](#cfn-macie-findingsfilter-findingcriteria)" : FindingCriteria,
      "[Name](#cfn-macie-findingsfilter-name)" : String,
      "[Position](#cfn-macie-findingsfilter-position)" : Integer
    }
}
```

### YAML<a name="aws-resource-macie-findingsfilter-syntax.yaml"></a>

```
Type: AWS::Macie::FindingsFilter
Properties: 
  [Action](#cfn-macie-findingsfilter-action): String
  [Description](#cfn-macie-findingsfilter-description): String
  [FindingCriteria](#cfn-macie-findingsfilter-findingcriteria): 
    FindingCriteria
  [Name](#cfn-macie-findingsfilter-name): String
  [Position](#cfn-macie-findingsfilter-position): Integer
```

## Properties<a name="aws-resource-macie-findingsfilter-properties"></a>

`Action`  <a name="cfn-macie-findingsfilter-action"></a>
The action to perform on findings that meet the filter criteria \(`FindingCriteria`\)\. Valid values are:  
+ ARCHIVE \- Suppress \(automatically archive\) the findings\.
+ NOOP \- Don't perform any action on the findings\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-macie-findingsfilter-description"></a>
A custom description of the filter\. The description can contain as many as 512 characters\.  
We strongly recommend that you avoid including any sensitive data in the description of a filter\. Other users might be able to see the filter's description, depending on the actions that they're allowed to perform in Amazon Macie\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingCriteria`  <a name="cfn-macie-findingsfilter-findingcriteria"></a>
The criteria to use to filter findings\.  
*Required*: Yes  
*Type*: [FindingCriteria](aws-properties-macie-findingsfilter-findingcriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-macie-findingsfilter-name"></a>
A custom name for the filter\. The name must contain at least 3 characters and can contain as many as 64 characters\.  
We strongly recommend that you avoid including any sensitive data in the name of a filter\. Other users might be able to see the filter's name, depending on the actions that they're allowed to perform in Amazon Macie\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-macie-findingsfilter-position"></a>
The position of the filter in the list of saved filters on the Amazon Macie console\. This value also determines the order in which the filter is applied to findings, relative to other filters that are also applied to the findings\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-macie-findingsfilter-return-values"></a>

### Ref<a name="aws-resource-macie-findingsfilter-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the `FindingsFilter`\. For example, `{ "Ref": "FindingsFilter" }`\.

### Fn::GetAtt<a name="aws-resource-macie-findingsfilter-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-macie-findingsfilter-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the filter\.

`FindingsFilterListItems`  <a name="FindingsFilterListItems-fn::getatt"></a>
An array of `FindingsFilterListItem` objects, one for each findings filter that's associated with the account\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the filter\.

## Examples<a name="aws-resource-macie-findingsfilter--examples"></a>

The following example demonstrates how to declare an `AWS::Macie::FindingsFilter` resource\.

### Creating a Macie FindingsFilter that filters by account ID<a name="aws-resource-macie-findingsfilter--examples--Creating_a_Macie_FindingsFilter_that_filters_by_account_ID"></a>

This example creates a findings filter that suppresses \(automatically archives\) findings that apply to the specified account\.

#### JSON<a name="aws-resource-macie-findingsfilter--examples--Creating_a_Macie_FindingsFilter_that_filters_by_account_ID--json"></a>

```
{
    "Type": "AWS::Macie::FindingsFilter",
    "DependsOn": "Session",
    "Properties": {
        "Action": "ARCHIVE",
        "Description": "My custom findings filter",
        "FindingCriteria": {
            "Criterion": {
                "AccountId": {
                    "eq": "123456789012"
                }
            }
        },
        "Name": "MyFilterName",
        "Position": 1
    }
}
```

#### YAML<a name="aws-resource-macie-findingsfilter--examples--Creating_a_Macie_FindingsFilter_that_filters_by_account_ID--yaml"></a>

```
Type: AWS::Macie::FindingsFilter
DependsOn: "Session"
Properties: 
    Action: ARCHIVE 
    Description: "My custom findings filter"
    FindingCriteria:
        Criterion:
            "AccountID": 
                eq: "123456789012" 
    Name: MyFilterName
    Position: 1
```