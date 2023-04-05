# AWS::QuickSight::Analysis ParameterDeclaration<a name="aws-properties-quicksight-analysis-parameterdeclaration"></a>

The declaration definition of a parameter\.

For more information, see [Parameters in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/parameters-in-quicksight.html) in the *Amazon QuickSight User Guide*\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-parameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-parameterdeclaration-syntax.json"></a>

```
{
  "[DateTimeParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-datetimeparameterdeclaration)" : DateTimeParameterDeclaration,
  "[DecimalParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-decimalparameterdeclaration)" : DecimalParameterDeclaration,
  "[IntegerParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-integerparameterdeclaration)" : IntegerParameterDeclaration,
  "[StringParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-stringparameterdeclaration)" : StringParameterDeclaration
}
```

### YAML<a name="aws-properties-quicksight-analysis-parameterdeclaration-syntax.yaml"></a>

```
  [DateTimeParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-datetimeparameterdeclaration): 
    DateTimeParameterDeclaration
  [DecimalParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-decimalparameterdeclaration): 
    DecimalParameterDeclaration
  [IntegerParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-integerparameterdeclaration): 
    IntegerParameterDeclaration
  [StringParameterDeclaration](#cfn-quicksight-analysis-parameterdeclaration-stringparameterdeclaration): 
    StringParameterDeclaration
```

## Properties<a name="aws-properties-quicksight-analysis-parameterdeclaration-properties"></a>

`DateTimeParameterDeclaration`  <a name="cfn-quicksight-analysis-parameterdeclaration-datetimeparameterdeclaration"></a>
A parameter declaration for the `DateTime` data type\.  
*Required*: No  
*Type*: [DateTimeParameterDeclaration](aws-properties-quicksight-analysis-datetimeparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalParameterDeclaration`  <a name="cfn-quicksight-analysis-parameterdeclaration-decimalparameterdeclaration"></a>
A parameter declaration for the `Decimal` data type\.  
*Required*: No  
*Type*: [DecimalParameterDeclaration](aws-properties-quicksight-analysis-decimalparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerParameterDeclaration`  <a name="cfn-quicksight-analysis-parameterdeclaration-integerparameterdeclaration"></a>
A parameter declaration for the `Integer` data type\.  
*Required*: No  
*Type*: [IntegerParameterDeclaration](aws-properties-quicksight-analysis-integerparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringParameterDeclaration`  <a name="cfn-quicksight-analysis-parameterdeclaration-stringparameterdeclaration"></a>
A parameter declaration for the `String` data type\.  
*Required*: No  
*Type*: [StringParameterDeclaration](aws-properties-quicksight-analysis-stringparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)