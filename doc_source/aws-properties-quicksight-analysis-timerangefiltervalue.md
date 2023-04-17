# AWS::QuickSight::Analysis TimeRangeFilterValue<a name="aws-properties-quicksight-analysis-timerangefiltervalue"></a>

The value of a time range filter\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-timerangefiltervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-timerangefiltervalue-syntax.json"></a>

```
{
  "[Parameter](#cfn-quicksight-analysis-timerangefiltervalue-parameter)" : String,
  "[RollingDate](#cfn-quicksight-analysis-timerangefiltervalue-rollingdate)" : RollingDateConfiguration,
  "[StaticValue](#cfn-quicksight-analysis-timerangefiltervalue-staticvalue)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-timerangefiltervalue-syntax.yaml"></a>

```
  [Parameter](#cfn-quicksight-analysis-timerangefiltervalue-parameter): String
  [RollingDate](#cfn-quicksight-analysis-timerangefiltervalue-rollingdate): 
    RollingDateConfiguration
  [StaticValue](#cfn-quicksight-analysis-timerangefiltervalue-staticvalue): String
```

## Properties<a name="aws-properties-quicksight-analysis-timerangefiltervalue-properties"></a>

`Parameter`  <a name="cfn-quicksight-analysis-timerangefiltervalue-parameter"></a>
The parameter type input value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RollingDate`  <a name="cfn-quicksight-analysis-timerangefiltervalue-rollingdate"></a>
The rolling date input value\.  
*Required*: No  
*Type*: [RollingDateConfiguration](aws-properties-quicksight-analysis-rollingdateconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValue`  <a name="cfn-quicksight-analysis-timerangefiltervalue-staticvalue"></a>
The static input value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)