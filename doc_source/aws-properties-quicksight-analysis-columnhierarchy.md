# AWS::QuickSight::Analysis ColumnHierarchy<a name="aws-properties-quicksight-analysis-columnhierarchy"></a>

The option that determines the hierarchy of the fields for a visual element\.

## Syntax<a name="aws-properties-quicksight-analysis-columnhierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-columnhierarchy-syntax.json"></a>

```
{
  "[DateTimeHierarchy](#cfn-quicksight-analysis-columnhierarchy-datetimehierarchy)" : DateTimeHierarchy,
  "[ExplicitHierarchy](#cfn-quicksight-analysis-columnhierarchy-explicithierarchy)" : ExplicitHierarchy,
  "[PredefinedHierarchy](#cfn-quicksight-analysis-columnhierarchy-predefinedhierarchy)" : PredefinedHierarchy
}
```

### YAML<a name="aws-properties-quicksight-analysis-columnhierarchy-syntax.yaml"></a>

```
  [DateTimeHierarchy](#cfn-quicksight-analysis-columnhierarchy-datetimehierarchy): 
    DateTimeHierarchy
  [ExplicitHierarchy](#cfn-quicksight-analysis-columnhierarchy-explicithierarchy): 
    ExplicitHierarchy
  [PredefinedHierarchy](#cfn-quicksight-analysis-columnhierarchy-predefinedhierarchy): 
    PredefinedHierarchy
```

## Properties<a name="aws-properties-quicksight-analysis-columnhierarchy-properties"></a>

`DateTimeHierarchy`  <a name="cfn-quicksight-analysis-columnhierarchy-datetimehierarchy"></a>
The option that determines the hierarchy of any `DateTime` fields\.  
*Required*: No  
*Type*: [DateTimeHierarchy](aws-properties-quicksight-analysis-datetimehierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplicitHierarchy`  <a name="cfn-quicksight-analysis-columnhierarchy-explicithierarchy"></a>
The option that determines the hierarchy of the fields that are built within a visual's field wells\. These fields can't be duplicated to other visuals\.  
*Required*: No  
*Type*: [ExplicitHierarchy](aws-properties-quicksight-analysis-explicithierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedHierarchy`  <a name="cfn-quicksight-analysis-columnhierarchy-predefinedhierarchy"></a>
The option that determines the hierarchy of the fields that are defined during data preparation\. These fields are available to use in any analysis that uses the data source\.  
*Required*: No  
*Type*: [PredefinedHierarchy](aws-properties-quicksight-analysis-predefinedhierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)