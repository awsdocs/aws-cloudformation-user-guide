# AWS::RDS::DBProxyEndpoint TagFormat<a name="aws-properties-rds-dbproxyendpoint-tagformat"></a>

Metadata assigned to a DB proxy endpoint consisting of a key\-value pair\.

## Syntax<a name="aws-properties-rds-dbproxyendpoint-tagformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbproxyendpoint-tagformat-syntax.json"></a>

```
{
  "[Key](#cfn-rds-dbproxyendpoint-tagformat-key)" : String,
  "[Value](#cfn-rds-dbproxyendpoint-tagformat-value)" : String
}
```

### YAML<a name="aws-properties-rds-dbproxyendpoint-tagformat-syntax.yaml"></a>

```
  [Key](#cfn-rds-dbproxyendpoint-tagformat-key): String
  [Value](#cfn-rds-dbproxyendpoint-tagformat-value): String
```

## Properties<a name="aws-properties-rds-dbproxyendpoint-tagformat-properties"></a>

`Key`  <a name="cfn-rds-dbproxyendpoint-tagformat-key"></a>
A value is the optional value of the tag\. The string value can be 1\-256 Unicode characters in length and can't be prefixed with `aws:`\. The string can contain only the set of Unicode letters, digits, white\-space, '\_', '\.', '/', '=', '\+', '\-' \(Java regex: "^\(\[\\\\p\{L\}\\\\p\{Z\}\\\\p\{N\}\_\.:/=\+\\\\\-\]\*\)$"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-rds-dbproxyendpoint-tagformat-value"></a>
Metadata assigned to a DB instance consisting of a key\-value pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)