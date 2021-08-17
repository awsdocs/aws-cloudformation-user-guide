# AWS::Kendra::DataSource AclConfiguration<a name="aws-properties-kendra-datasource-aclconfiguration"></a>

Provides information about the column that should be used for filtering the query response by groups\.

## Syntax<a name="aws-properties-kendra-datasource-aclconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-aclconfiguration-syntax.json"></a>

```
{
  "[AllowedGroupsColumnName](#cfn-kendra-datasource-aclconfiguration-allowedgroupscolumnname)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-aclconfiguration-syntax.yaml"></a>

```
  [AllowedGroupsColumnName](#cfn-kendra-datasource-aclconfiguration-allowedgroupscolumnname): String
```

## Properties<a name="aws-properties-kendra-datasource-aclconfiguration-properties"></a>

`AllowedGroupsColumnName`  <a name="cfn-kendra-datasource-aclconfiguration-allowedgroupscolumnname"></a>
A list of groups, separated by semi\-colons, that filters a query response based on user context\. The document is only returned to users that are in one of the groups specified in the `UserContext` field of the [Query](https://docs.aws.amazon.com/kendra/latest/dg/API_Query.html) operation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)