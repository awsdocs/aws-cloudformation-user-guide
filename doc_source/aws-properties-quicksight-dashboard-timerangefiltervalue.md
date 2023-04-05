# AWS::QuickSight::Dashboard TimeRangeFilterValue<a name="aws-properties-quicksight-dashboard-timerangefiltervalue"></a>

The value of a time range filter\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-timerangefiltervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-timerangefiltervalue-syntax.json"></a>

```
{
  "[Parameter](#cfn-quicksight-dashboard-timerangefiltervalue-parameter)" : String,
  "[RollingDate](#cfn-quicksight-dashboard-timerangefiltervalue-rollingdate)" : RollingDateConfiguration,
  "[StaticValue](#cfn-quicksight-dashboard-timerangefiltervalue-staticvalue)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-timerangefiltervalue-syntax.yaml"></a>

```
  [Parameter](#cfn-quicksight-dashboard-timerangefiltervalue-parameter): String
  [RollingDate](#cfn-quicksight-dashboard-timerangefiltervalue-rollingdate): 
    RollingDateConfiguration
  [StaticValue](#cfn-quicksight-dashboard-timerangefiltervalue-staticvalue): String
```

## Properties<a name="aws-properties-quicksight-dashboard-timerangefiltervalue-properties"></a>

`Parameter`  <a name="cfn-quicksight-dashboard-timerangefiltervalue-parameter"></a>
The parameter type input value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RollingDate`  <a name="cfn-quicksight-dashboard-timerangefiltervalue-rollingdate"></a>
The rolling date input value\.  
*Required*: No  
*Type*: [RollingDateConfiguration](aws-properties-quicksight-dashboard-rollingdateconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValue`  <a name="cfn-quicksight-dashboard-timerangefiltervalue-staticvalue"></a>
The static input value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)