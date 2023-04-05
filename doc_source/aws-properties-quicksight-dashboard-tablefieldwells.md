# AWS::QuickSight::Dashboard TableFieldWells<a name="aws-properties-quicksight-dashboard-tablefieldwells"></a>

The field wells for a table visual\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablefieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablefieldwells-syntax.json"></a>

```
{
  "[TableAggregatedFieldWells](#cfn-quicksight-dashboard-tablefieldwells-tableaggregatedfieldwells)" : TableAggregatedFieldWells,
  "[TableUnaggregatedFieldWells](#cfn-quicksight-dashboard-tablefieldwells-tableunaggregatedfieldwells)" : TableUnaggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablefieldwells-syntax.yaml"></a>

```
  [TableAggregatedFieldWells](#cfn-quicksight-dashboard-tablefieldwells-tableaggregatedfieldwells): 
    TableAggregatedFieldWells
  [TableUnaggregatedFieldWells](#cfn-quicksight-dashboard-tablefieldwells-tableunaggregatedfieldwells): 
    TableUnaggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-dashboard-tablefieldwells-properties"></a>

`TableAggregatedFieldWells`  <a name="cfn-quicksight-dashboard-tablefieldwells-tableaggregatedfieldwells"></a>
The aggregated field well for the table\.  
*Required*: No  
*Type*: [TableAggregatedFieldWells](aws-properties-quicksight-dashboard-tableaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableUnaggregatedFieldWells`  <a name="cfn-quicksight-dashboard-tablefieldwells-tableunaggregatedfieldwells"></a>
The unaggregated field well for the table\.  
*Required*: No  
*Type*: [TableUnaggregatedFieldWells](aws-properties-quicksight-dashboard-tableunaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)