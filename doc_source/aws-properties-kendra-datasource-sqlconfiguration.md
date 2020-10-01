# AWS::Kendra::DataSource SqlConfiguration<a name="aws-properties-kendra-datasource-sqlconfiguration"></a>

Provides information that configures Amazon Kendra to use a SQL database\.

## Syntax<a name="aws-properties-kendra-datasource-sqlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-sqlconfiguration-syntax.json"></a>

```
{
  "[QueryIdentifiersEnclosingOption](#cfn-kendra-datasource-sqlconfiguration-queryidentifiersenclosingoption)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-sqlconfiguration-syntax.yaml"></a>

```
  [QueryIdentifiersEnclosingOption](#cfn-kendra-datasource-sqlconfiguration-queryidentifiersenclosingoption): String
```

## Properties<a name="aws-properties-kendra-datasource-sqlconfiguration-properties"></a>

`QueryIdentifiersEnclosingOption`  <a name="cfn-kendra-datasource-sqlconfiguration-queryidentifiersenclosingoption"></a>
Determines whether Amazon Kendra encloses SQL identifiers for tables and column names in double quotes \("\) when making a database query\. You can set the value to `DOUBLE_QUOTES` or `NONE`\.  
 By default, Amazon Kendra passes SQL identifiers the way that they are entered into the data source configuration\. It does not change the case of identifiers or enclose them in quotes\.  
 PostgreSQL internally converts uppercase characters to lower case characters in identifiers unless they are quoted\. Choosing this option encloses identifiers in quotes so that PostgreSQL does not convert the character's case\.  
 For MySQL databases, you must enable the ansi\_quotes option when you set this field to `DOUBLE_QUOTES`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)