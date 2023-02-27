# AWS::LakeFormation::DataCellsFilter ColumnWildcard<a name="aws-properties-lakeformation-datacellsfilter-columnwildcard"></a>

A wildcard object, consisting of an optional list of excluded column names or indexes\.

## Syntax<a name="aws-properties-lakeformation-datacellsfilter-columnwildcard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-datacellsfilter-columnwildcard-syntax.json"></a>

```
{
  "[ExcludedColumnNames](#cfn-lakeformation-datacellsfilter-columnwildcard-excludedcolumnnames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lakeformation-datacellsfilter-columnwildcard-syntax.yaml"></a>

```
  [ExcludedColumnNames](#cfn-lakeformation-datacellsfilter-columnwildcard-excludedcolumnnames): 
    - String
```

## Properties<a name="aws-properties-lakeformation-datacellsfilter-columnwildcard-properties"></a>

`ExcludedColumnNames`  <a name="cfn-lakeformation-datacellsfilter-columnwildcard-excludedcolumnnames"></a>
Excludes column names\. Any column with this name will be excluded\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)