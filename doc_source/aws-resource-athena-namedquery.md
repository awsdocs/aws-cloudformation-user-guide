# AWS::Athena::NamedQuery<a name="aws-resource-athena-namedquery"></a>

The AWS::Athena::NamedQuery resource specifies an Amazon Athena query, where `QueryString` is the list of SQL query statements that comprise the query\. For more information, see [CreateNamedQuery](https://docs.aws.amazon.com/athena/latest/APIReference/API_CreateNamedQuery.html) in the *Amazon Athena API Reference*\. 

## Syntax<a name="aws-resource-athena-namedquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-athena-namedquery-syntax.json"></a>

```
{
  "Type" : "AWS::Athena::NamedQuery",
  "Properties" : {
      "[Database](#cfn-athena-namedquery-database)" : String,
      "[Description](#cfn-athena-namedquery-description)" : String,
      "[Name](#cfn-athena-namedquery-name)" : String,
      "[QueryString](#cfn-athena-namedquery-querystring)" : String
    }
}
```

### YAML<a name="aws-resource-athena-namedquery-syntax.yaml"></a>

```
Type: AWS::Athena::NamedQuery
Properties: 
  [Database](#cfn-athena-namedquery-database): String
  [Description](#cfn-athena-namedquery-description): String
  [Name](#cfn-athena-namedquery-name): String
  [QueryString](#cfn-athena-namedquery-querystring): 
    String
```

## Properties<a name="aws-resource-athena-namedquery-properties"></a>

`Database`  <a name="cfn-athena-namedquery-database"></a>
The database to which the query belongs\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-athena-namedquery-description"></a>
The query description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-athena-namedquery-name"></a>
The query name\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QueryString`  <a name="cfn-athena-namedquery-querystring"></a>
The SQL query statements that comprise the query\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `262144`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-athena-namedquery-return-values"></a>

### Ref<a name="aws-resource-athena-namedquery-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-athena-namedquery--examples"></a>

The following example creates a named query\.

### <a name="aws-resource-athena-namedquery--examples--"></a>

#### JSON<a name="aws-resource-athena-namedquery--examples----json"></a>

```
{
  "Resources": {
    "AthenaNamedQuery": {
      "Type": "AWS::Athena::NamedQuery",
      "Properties": {
        "Database": "swfnetadata",
        "Description": "A query that selects all aggregated data",
        "Name": "MostExpensiveWorkflow",
        "QueryString": "SELECT workflowname, AVG(activitytaskstarted) AS AverageWorkflow FROM swfmetadata WHERE year='17' AND GROUP BY workflowname ORDER BY AverageWorkflow DESC LIMIT 10"
      }
    }
  }
}
```

### <a name="aws-resource-athena-namedquery--examples--"></a>

#### YAML<a name="aws-resource-athena-namedquery--examples----yaml"></a>

```
Resources:
  AthenaNamedQuery:
    Type: AWS::Athena::NamedQuery
    Properties:
      Database: "swfnetadata"
      Description: "A query that selects all aggregated data"
      Name: "MostExpensiveWorkflow"
      QueryString: >
                    SELECT workflowname, AVG(activitytaskstarted) AS AverageWorkflow
                    FROM swfmetadata
                    WHERE year='17' AND GROUP BY workflowname
                    ORDER BY AverageWorkflow DESC LIMIT 10
```