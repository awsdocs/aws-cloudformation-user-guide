# AWS::Athena::NamedQuery<a name="aws-resource-athena-namedquery"></a>

The `AWS::Athena::NamedQuery` resource specifies an Amazon Athena saved query, where `QueryString` is the list of SQL query statements that comprise the query\.

**Note**  
The `AWS::Athena::NamedQuery` resource creates a named query in the primary workgroup\. To create a named query in a different workgroup, use the [CreateNamedQuery](https://docs.aws.amazon.com/athena/latest/APIReference/API_CreateNamedQuery.html) API operation and specify a workgroup in the `WorkGroup` parameter, or use the [create\-named\-query](https://docs.aws.amazon.com/cli/latest/reference/athena/create-named-query.html) AWS CLI command and specify a workgroup in the `--work-group` option\.

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
      "[QueryString](#cfn-athena-namedquery-querystring)" : String,
      "[WorkGroup](#cfn-athena-namedquery-workgroup)" : String
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
  [WorkGroup](#cfn-athena-namedquery-workgroup): String
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

`WorkGroup`  <a name="cfn-athena-namedquery-workgroup"></a>
The name of the workgroup that contains the named query\.  
*Required*: No  
*Type*: String  
*Pattern*: `[a-zA-Z0-9._-]{1,128}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-athena-namedquery-return-values"></a>

### Ref<a name="aws-resource-athena-namedquery-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-athena-namedquery-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-athena-namedquery-return-values-fn--getatt-fn--getatt"></a>

`NamedQueryId`  <a name="NamedQueryId-fn::getatt"></a>
The unique ID of the query\.

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