# AWS::Kendra::DataSource ExcludeSharedDrivesList<a name="aws-properties-kendra-datasource-excludeshareddriveslist"></a>

A list of shared Google drives to exclude from an Amazon Kendra index\.

## Syntax<a name="aws-properties-kendra-datasource-excludeshareddriveslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-excludeshareddriveslist-syntax.json"></a>

```
{
  "[ExcludeSharedDrivesList](#cfn-kendra-datasource-excludeshareddriveslist-excludeshareddriveslist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-excludeshareddriveslist-syntax.yaml"></a>

```
  [ExcludeSharedDrivesList](#cfn-kendra-datasource-excludeshareddriveslist-excludeshareddriveslist): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-excludeshareddriveslist-properties"></a>

`ExcludeSharedDrivesList`  <a name="cfn-kendra-datasource-excludeshareddriveslist-excludeshareddriveslist"></a>
A list of strings that define the shared Google drives to exclude from an Amazon Kendra index\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-excludeshareddriveslist) of [String](#aws-properties-kendra-datasource-excludeshareddriveslist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)