# AWS::QuickSight::Dashboard ParameterDeclaration<a name="aws-properties-quicksight-dashboard-parameterdeclaration"></a>

The declaration definition of a parameter\.

For more information, see [Parameters in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/parameters-in-quicksight.html) in the *Amazon QuickSight User Guide*\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-parameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parameterdeclaration-syntax.json"></a>

```
{
  "[DateTimeParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-datetimeparameterdeclaration)" : DateTimeParameterDeclaration,
  "[DecimalParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-decimalparameterdeclaration)" : DecimalParameterDeclaration,
  "[IntegerParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-integerparameterdeclaration)" : IntegerParameterDeclaration,
  "[StringParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-stringparameterdeclaration)" : StringParameterDeclaration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parameterdeclaration-syntax.yaml"></a>

```
  [DateTimeParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-datetimeparameterdeclaration): 
    DateTimeParameterDeclaration
  [DecimalParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-decimalparameterdeclaration): 
    DecimalParameterDeclaration
  [IntegerParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-integerparameterdeclaration): 
    IntegerParameterDeclaration
  [StringParameterDeclaration](#cfn-quicksight-dashboard-parameterdeclaration-stringparameterdeclaration): 
    StringParameterDeclaration
```

## Properties<a name="aws-properties-quicksight-dashboard-parameterdeclaration-properties"></a>

`DateTimeParameterDeclaration`  <a name="cfn-quicksight-dashboard-parameterdeclaration-datetimeparameterdeclaration"></a>
A parameter declaration for the `DateTime` data type\.  
*Required*: No  
*Type*: [DateTimeParameterDeclaration](aws-properties-quicksight-dashboard-datetimeparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalParameterDeclaration`  <a name="cfn-quicksight-dashboard-parameterdeclaration-decimalparameterdeclaration"></a>
A parameter declaration for the `Decimal` data type\.  
*Required*: No  
*Type*: [DecimalParameterDeclaration](aws-properties-quicksight-dashboard-decimalparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerParameterDeclaration`  <a name="cfn-quicksight-dashboard-parameterdeclaration-integerparameterdeclaration"></a>
A parameter declaration for the `Integer` data type\.  
*Required*: No  
*Type*: [IntegerParameterDeclaration](aws-properties-quicksight-dashboard-integerparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringParameterDeclaration`  <a name="cfn-quicksight-dashboard-parameterdeclaration-stringparameterdeclaration"></a>
A parameter declaration for the `String` data type\.  
*Required*: No  
*Type*: [StringParameterDeclaration](aws-properties-quicksight-dashboard-stringparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)