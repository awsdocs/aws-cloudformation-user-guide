# AWS::Athena::PreparedStatement<a name="aws-resource-athena-preparedstatement"></a>

Specifies a prepared statement for use with SQL queries in Athena\.

## Syntax<a name="aws-resource-athena-preparedstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-athena-preparedstatement-syntax.json"></a>

```
{
  "Type" : "AWS::Athena::PreparedStatement",
  "Properties" : {
      "[Description](#cfn-athena-preparedstatement-description)" : String,
      "[QueryStatement](#cfn-athena-preparedstatement-querystatement)" : String,
      "[StatementName](#cfn-athena-preparedstatement-statementname)" : String,
      "[WorkGroup](#cfn-athena-preparedstatement-workgroup)" : String
    }
}
```

### YAML<a name="aws-resource-athena-preparedstatement-syntax.yaml"></a>

```
Type: AWS::Athena::PreparedStatement
Properties: 
  [Description](#cfn-athena-preparedstatement-description): String
  [QueryStatement](#cfn-athena-preparedstatement-querystatement): String
  [StatementName](#cfn-athena-preparedstatement-statementname): String
  [WorkGroup](#cfn-athena-preparedstatement-workgroup): String
```

## Properties<a name="aws-resource-athena-preparedstatement-properties"></a>

`Description`  <a name="cfn-athena-preparedstatement-description"></a>
The description of the prepared statement\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStatement`  <a name="cfn-athena-preparedstatement-querystatement"></a>
The query string for the prepared statement\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `262144`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatementName`  <a name="cfn-athena-preparedstatement-statementname"></a>
The name of the prepared statement\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WorkGroup`  <a name="cfn-athena-preparedstatement-workgroup"></a>
The workgroup to which the prepared statement belongs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-athena-preparedstatement-return-values"></a>

### Ref<a name="aws-resource-athena-preparedstatement-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the prepared statement\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.