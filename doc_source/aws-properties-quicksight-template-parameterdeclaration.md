# AWS::QuickSight::Template ParameterDeclaration<a name="aws-properties-quicksight-template-parameterdeclaration"></a>

The declaration definition of a parameter\.

For more information, see [Parameters in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/parameters-in-quicksight.html) in the *Amazon QuickSight User Guide*\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-parameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-parameterdeclaration-syntax.json"></a>

```
{
  "[DateTimeParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-datetimeparameterdeclaration)" : DateTimeParameterDeclaration,
  "[DecimalParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-decimalparameterdeclaration)" : DecimalParameterDeclaration,
  "[IntegerParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-integerparameterdeclaration)" : IntegerParameterDeclaration,
  "[StringParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-stringparameterdeclaration)" : StringParameterDeclaration
}
```

### YAML<a name="aws-properties-quicksight-template-parameterdeclaration-syntax.yaml"></a>

```
  [DateTimeParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-datetimeparameterdeclaration): 
    DateTimeParameterDeclaration
  [DecimalParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-decimalparameterdeclaration): 
    DecimalParameterDeclaration
  [IntegerParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-integerparameterdeclaration): 
    IntegerParameterDeclaration
  [StringParameterDeclaration](#cfn-quicksight-template-parameterdeclaration-stringparameterdeclaration): 
    StringParameterDeclaration
```

## Properties<a name="aws-properties-quicksight-template-parameterdeclaration-properties"></a>

`DateTimeParameterDeclaration`  <a name="cfn-quicksight-template-parameterdeclaration-datetimeparameterdeclaration"></a>
A parameter declaration for the `DateTime` data type\.  
*Required*: No  
*Type*: [DateTimeParameterDeclaration](aws-properties-quicksight-template-datetimeparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalParameterDeclaration`  <a name="cfn-quicksight-template-parameterdeclaration-decimalparameterdeclaration"></a>
A parameter declaration for the `Decimal` data type\.  
*Required*: No  
*Type*: [DecimalParameterDeclaration](aws-properties-quicksight-template-decimalparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerParameterDeclaration`  <a name="cfn-quicksight-template-parameterdeclaration-integerparameterdeclaration"></a>
A parameter declaration for the `Integer` data type\.  
*Required*: No  
*Type*: [IntegerParameterDeclaration](aws-properties-quicksight-template-integerparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringParameterDeclaration`  <a name="cfn-quicksight-template-parameterdeclaration-stringparameterdeclaration"></a>
A parameter declaration for the `String` data type\.  
*Required*: No  
*Type*: [StringParameterDeclaration](aws-properties-quicksight-template-stringparameterdeclaration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)