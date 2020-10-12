# AWS::RDS::DBProxy TagFormat<a name="aws-properties-rds-dbproxy-tagformat"></a>

Metadata assigned to a DB instance consisting of a key\-value pair\.

## Syntax<a name="aws-properties-rds-dbproxy-tagformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbproxy-tagformat-syntax.json"></a>

```
{
  "[Key](#cfn-rds-dbproxy-tagformat-key)" : String,
  "[Value](#cfn-rds-dbproxy-tagformat-value)" : String
}
```

### YAML<a name="aws-properties-rds-dbproxy-tagformat-syntax.yaml"></a>

```
  [Key](#cfn-rds-dbproxy-tagformat-key): String
  [Value](#cfn-rds-dbproxy-tagformat-value): String
```

## Properties<a name="aws-properties-rds-dbproxy-tagformat-properties"></a>

`Key`  <a name="cfn-rds-dbproxy-tagformat-key"></a>
A key is the required name of the tag\. The string value can be 1\-128 Unicode characters in length and can't be prefixed with "aws:"\. The string can contain only the set of Unicode letters, digits, white\-space, '\_', '\.', '/', '=', '\+', '\-' \(Java regex: "^\(\[\\\\p\{L\}\\\\p\{Z\}\\\\p\{N\}\_\.:/=\+\\\\\-\]\*\)$"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-rds-dbproxy-tagformat-value"></a>
A value is the optional value of the tag\. The string value can be 1\-256 Unicode characters in length and can't be prefixed with "aws:"\. The string can contain only the set of Unicode letters, digits, white\-space, '\_', '\.', '/', '=', '\+', '\-' \(Java regex: "^\(\[\\\\p\{L\}\\\\p\{Z\}\\\\p\{N\}\_\.:/=\+\\\\\-\]\*\)$"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)