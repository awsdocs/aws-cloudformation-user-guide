# AWS::Kendra::DataSource ConfluenceSpaceList<a name="aws-properties-kendra-datasource-confluencespacelist"></a>

A list of Confluence spaces to include or exclude from an Amazon Kendra index\.

## Syntax<a name="aws-properties-kendra-datasource-confluencespacelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencespacelist-syntax.json"></a>

```
{
  "[ConfluenceSpaceList](#cfn-kendra-datasource-confluencespacelist-confluencespacelist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencespacelist-syntax.yaml"></a>

```
  [ConfluenceSpaceList](#cfn-kendra-datasource-confluencespacelist-confluencespacelist): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-confluencespacelist-properties"></a>

`ConfluenceSpaceList`  <a name="cfn-kendra-datasource-confluencespacelist-confluencespacelist"></a>
A list of Confluence spaces\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-confluencespacelist) of [String](#aws-properties-kendra-datasource-confluencespacelist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)