# AWS::QuickSight::Dashboard ColumnHierarchy<a name="aws-properties-quicksight-dashboard-columnhierarchy"></a>

The option that determines the hierarchy of the fields for a visual element\.

## Syntax<a name="aws-properties-quicksight-dashboard-columnhierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-columnhierarchy-syntax.json"></a>

```
{
  "[DateTimeHierarchy](#cfn-quicksight-dashboard-columnhierarchy-datetimehierarchy)" : DateTimeHierarchy,
  "[ExplicitHierarchy](#cfn-quicksight-dashboard-columnhierarchy-explicithierarchy)" : ExplicitHierarchy,
  "[PredefinedHierarchy](#cfn-quicksight-dashboard-columnhierarchy-predefinedhierarchy)" : PredefinedHierarchy
}
```

### YAML<a name="aws-properties-quicksight-dashboard-columnhierarchy-syntax.yaml"></a>

```
  [DateTimeHierarchy](#cfn-quicksight-dashboard-columnhierarchy-datetimehierarchy): 
    DateTimeHierarchy
  [ExplicitHierarchy](#cfn-quicksight-dashboard-columnhierarchy-explicithierarchy): 
    ExplicitHierarchy
  [PredefinedHierarchy](#cfn-quicksight-dashboard-columnhierarchy-predefinedhierarchy): 
    PredefinedHierarchy
```

## Properties<a name="aws-properties-quicksight-dashboard-columnhierarchy-properties"></a>

`DateTimeHierarchy`  <a name="cfn-quicksight-dashboard-columnhierarchy-datetimehierarchy"></a>
The option that determines the hierarchy of any `DateTime` fields\.  
*Required*: No  
*Type*: [DateTimeHierarchy](aws-properties-quicksight-dashboard-datetimehierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplicitHierarchy`  <a name="cfn-quicksight-dashboard-columnhierarchy-explicithierarchy"></a>
The option that determines the hierarchy of the fields that are built within a visual's field wells\. These fields can't be duplicated to other visuals\.  
*Required*: No  
*Type*: [ExplicitHierarchy](aws-properties-quicksight-dashboard-explicithierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredefinedHierarchy`  <a name="cfn-quicksight-dashboard-columnhierarchy-predefinedhierarchy"></a>
The option that determines the hierarchy of the fields that are defined during data preparation\. These fields are available to use in any analysis that uses the data source\.  
*Required*: No  
*Type*: [PredefinedHierarchy](aws-properties-quicksight-dashboard-predefinedhierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)