# AWS::Kendra::DataSource DataSourceInclusionsExclusionsStrings<a name="aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings"></a>

Regular expressions that include or exclude documents from the data source\.

## Syntax<a name="aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings-syntax.json"></a>

```
{
  "[DataSourceInclusionsExclusionsStrings](#cfn-kendra-datasource-datasourceinclusionsexclusionsstrings-datasourceinclusionsexclusionsstrings)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings-syntax.yaml"></a>

```
  [DataSourceInclusionsExclusionsStrings](#cfn-kendra-datasource-datasourceinclusionsexclusionsstrings-datasourceinclusionsexclusionsstrings): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings-properties"></a>

`DataSourceInclusionsExclusionsStrings`  <a name="cfn-kendra-datasource-datasourceinclusionsexclusionsstrings-datasourceinclusionsexclusionsstrings"></a>
A list of regular expressions that include or exclude documents from the data source\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings) of [String](#aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)