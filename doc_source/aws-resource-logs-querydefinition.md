# AWS::Logs::QueryDefinition<a name="aws-resource-logs-querydefinition"></a>

Creates a query definition for CloudWatch Logs Insights\. For more information, see [ Analyzing Log Data with CloudWatch Logs Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html)\.

## Syntax<a name="aws-resource-logs-querydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-querydefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::QueryDefinition",
  "Properties" : {
      "[LogGroupNames](#cfn-logs-querydefinition-loggroupnames)" : [ String, ... ],
      "[Name](#cfn-logs-querydefinition-name)" : String,
      "[QueryString](#cfn-logs-querydefinition-querystring)" : String
    }
}
```

### YAML<a name="aws-resource-logs-querydefinition-syntax.yaml"></a>

```
Type: AWS::Logs::QueryDefinition
Properties: 
  [LogGroupNames](#cfn-logs-querydefinition-loggroupnames): 
    - String
  [Name](#cfn-logs-querydefinition-name): String
  [QueryString](#cfn-logs-querydefinition-querystring): 
    String
```

## Properties<a name="aws-resource-logs-querydefinition-properties"></a>

`LogGroupNames`  <a name="cfn-logs-querydefinition-loggroupnames"></a>
Use this parameter if you want the query to query only certain log groups\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-logs-querydefinition-name"></a>
A name for the query definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-logs-querydefinition-querystring"></a>
The query string to use for this query definition\. For more information, see [ CloudWatch Logs Insights Query Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-logs-querydefinition-return-values"></a>

### Ref<a name="aws-resource-logs-querydefinition-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the query definition ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-logs-querydefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-logs-querydefinition-return-values-fn--getatt-fn--getatt"></a>

`QueryDefinitionId`  <a name="QueryDefinitionId-fn::getatt"></a>
The ID of the query definition\. 

## Examples<a name="aws-resource-logs-querydefinition--examples"></a>

### Query definition example<a name="aws-resource-logs-querydefinition--examples--Query_definition_example"></a>

The following example creates a query definition\.

#### JSON<a name="aws-resource-logs-querydefinition--examples--Query_definition_example--json"></a>

```
"myQueryDefinition": {
  "Type": "AWS::Logs::QueryDefinition",
  "Properties": {
    "Name": "myQueryName",
    "QueryString": "fields @timestamp, @message | sort @timestamp desc | limit 20"
    }
}
```

#### YAML<a name="aws-resource-logs-querydefinition--examples--Query_definition_example--yaml"></a>

```
myQueryDefinition:
  Type: AWS::Logs::QueryDefinition
  Properties:
    Name: "myQueryName"
    QueryString: “fields @timestamp, @message | sort @timestamp desc | limit 20"
```