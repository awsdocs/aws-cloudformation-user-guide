# AWS::DataBrew::Ruleset ColumnSelector<a name="aws-properties-databrew-ruleset-columnselector"></a>

Selector of a column from a dataset for profile job configuration\. One selector includes either a column name or a regular expression\.

## Syntax<a name="aws-properties-databrew-ruleset-columnselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-ruleset-columnselector-syntax.json"></a>

```
{
  "[Name](#cfn-databrew-ruleset-columnselector-name)" : String,
  "[Regex](#cfn-databrew-ruleset-columnselector-regex)" : String
}
```

### YAML<a name="aws-properties-databrew-ruleset-columnselector-syntax.yaml"></a>

```
  [Name](#cfn-databrew-ruleset-columnselector-name): String
  [Regex](#cfn-databrew-ruleset-columnselector-regex): String
```

## Properties<a name="aws-properties-databrew-ruleset-columnselector-properties"></a>

`Name`  <a name="cfn-databrew-ruleset-columnselector-name"></a>
The name of a column from a dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regex`  <a name="cfn-databrew-ruleset-columnselector-regex"></a>
A regular expression for selecting a column from a dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)