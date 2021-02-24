# AWS::Kendra::DataSource ExcludeMimeTypesList<a name="aws-properties-kendra-datasource-excludemimetypeslist"></a>

A list of MIME types from a Google Drive data source to exclude from the Amazon Kendra index\.

## Syntax<a name="aws-properties-kendra-datasource-excludemimetypeslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-excludemimetypeslist-syntax.json"></a>

```
{
  "[ExcludeMimeTypesList](#cfn-kendra-datasource-excludemimetypeslist-excludemimetypeslist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-excludemimetypeslist-syntax.yaml"></a>

```
  [ExcludeMimeTypesList](#cfn-kendra-datasource-excludemimetypeslist-excludemimetypeslist): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-excludemimetypeslist-properties"></a>

`ExcludeMimeTypesList`  <a name="cfn-kendra-datasource-excludemimetypeslist-excludemimetypeslist"></a>
A list of strings that define the MIME types from a Google Drive data source to exclude from an Amazon Kendra index\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-excludemimetypeslist) of [String](#aws-properties-kendra-datasource-excludemimetypeslist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)