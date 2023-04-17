# AWS::QuickSight::Analysis GlobalTableBorderOptions<a name="aws-properties-quicksight-analysis-globaltableborderoptions"></a>

Determines the border options for a table visual\.

## Syntax<a name="aws-properties-quicksight-analysis-globaltableborderoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-globaltableborderoptions-syntax.json"></a>

```
{
  "[SideSpecificBorder](#cfn-quicksight-analysis-globaltableborderoptions-sidespecificborder)" : TableSideBorderOptions,
  "[UniformBorder](#cfn-quicksight-analysis-globaltableborderoptions-uniformborder)" : TableBorderOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-globaltableborderoptions-syntax.yaml"></a>

```
  [SideSpecificBorder](#cfn-quicksight-analysis-globaltableborderoptions-sidespecificborder): 
    TableSideBorderOptions
  [UniformBorder](#cfn-quicksight-analysis-globaltableborderoptions-uniformborder): 
    TableBorderOptions
```

## Properties<a name="aws-properties-quicksight-analysis-globaltableborderoptions-properties"></a>

`SideSpecificBorder`  <a name="cfn-quicksight-analysis-globaltableborderoptions-sidespecificborder"></a>
Determines the options for side specific border\.  
*Required*: No  
*Type*: [TableSideBorderOptions](aws-properties-quicksight-analysis-tablesideborderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UniformBorder`  <a name="cfn-quicksight-analysis-globaltableborderoptions-uniformborder"></a>
Determines the options for uniform border\.  
*Required*: No  
*Type*: [TableBorderOptions](aws-properties-quicksight-analysis-tableborderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)