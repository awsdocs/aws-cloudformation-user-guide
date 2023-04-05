# AWS::QuickSight::Template TableFieldWells<a name="aws-properties-quicksight-template-tablefieldwells"></a>

The field wells for a table visual\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-tablefieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablefieldwells-syntax.json"></a>

```
{
  "[TableAggregatedFieldWells](#cfn-quicksight-template-tablefieldwells-tableaggregatedfieldwells)" : TableAggregatedFieldWells,
  "[TableUnaggregatedFieldWells](#cfn-quicksight-template-tablefieldwells-tableunaggregatedfieldwells)" : TableUnaggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-template-tablefieldwells-syntax.yaml"></a>

```
  [TableAggregatedFieldWells](#cfn-quicksight-template-tablefieldwells-tableaggregatedfieldwells): 
    TableAggregatedFieldWells
  [TableUnaggregatedFieldWells](#cfn-quicksight-template-tablefieldwells-tableunaggregatedfieldwells): 
    TableUnaggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-template-tablefieldwells-properties"></a>

`TableAggregatedFieldWells`  <a name="cfn-quicksight-template-tablefieldwells-tableaggregatedfieldwells"></a>
The aggregated field well for the table\.  
*Required*: No  
*Type*: [TableAggregatedFieldWells](aws-properties-quicksight-template-tableaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableUnaggregatedFieldWells`  <a name="cfn-quicksight-template-tablefieldwells-tableunaggregatedfieldwells"></a>
The unaggregated field well for the table\.  
*Required*: No  
*Type*: [TableUnaggregatedFieldWells](aws-properties-quicksight-template-tableunaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)