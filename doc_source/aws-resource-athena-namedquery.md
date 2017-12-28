# AWS::Athena::NamedQuery<a name="aws-resource-athena-namedquery"></a>

The `AWS::Athena::NamedQuery` resource creates an Amazon Athena query\. For more information, see [CreateNamedQuery](http://docs.aws.amazon.com/athena/latest/APIReference/API_CreateNamedQuery.html) in the *Amazon Athena Documentation*\.


+ [Syntax](#aws-resource-athena-namedquery-syntax)
+ [Properties](#aws-resource-athena-namedquery-properties)
+ [Return Values](#aws-resource-athena-namedquery-returnvalues)
+ [Examples](#aws-resource-athena-namedquery-examples)

## Syntax<a name="aws-resource-athena-namedquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-athena-namedquery-syntax.json"></a>

```
{
  "Type" : "AWS::Athena::NamedQuery",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-querystring)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-database)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-name)" : String
  }
}
```

### YAML<a name="aws-resource-athena-namedquery-syntax.yaml"></a>

```
Type: "AWS::Athena::NamedQuery"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-querystring): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-database): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-athena-namedquery-name): String
```

## Properties<a name="aws-resource-athena-namedquery-properties"></a>

For constraints, see [NamedQuery](http://docs.aws.amazon.com/athena/latest/APIReference/API_NamedQuery.html) in the *Amazon Athena API Reference*\.

`Description`  
A brief description of the query\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`QueryString`  
The SQL query statements that comprise the query\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Database`  
The database to which the query belongs\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The plain\-language name of the query\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

## Return Values<a name="aws-resource-athena-namedquery-returnvalues"></a>

### Ref<a name="w3ab2c21c10d104c11b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\. 

## Examples<a name="aws-resource-athena-namedquery-examples"></a>

### <a name="aws-resource-athena-namedquery-example1"></a>

The following example creates a named query\.

#### JSON<a name="aws-resource-athena-namedquery-example1.json"></a>

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

#### YAML<a name="aws-resource-athena-namedquery-example1.yaml"></a>

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