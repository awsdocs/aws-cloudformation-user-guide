# AWS::QuickSight::Dashboard NullValueFormatConfiguration<a name="aws-properties-quicksight-dashboard-nullvalueformatconfiguration"></a>

The options that determine the null value format configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-nullvalueformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-nullvalueformatconfiguration-syntax.json"></a>

```
{
  "[NullString](#cfn-quicksight-dashboard-nullvalueformatconfiguration-nullstring)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-nullvalueformatconfiguration-syntax.yaml"></a>

```
  [NullString](#cfn-quicksight-dashboard-nullvalueformatconfiguration-nullstring): 
    String
```

## Properties<a name="aws-properties-quicksight-dashboard-nullvalueformatconfiguration-properties"></a>

`NullString`  <a name="cfn-quicksight-dashboard-nullvalueformatconfiguration-nullstring"></a>
Determines the null string of null values\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)