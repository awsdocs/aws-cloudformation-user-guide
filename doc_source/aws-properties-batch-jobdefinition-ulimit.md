# AWS Batch JobDefinition Ulimit<a name="aws-properties-batch-jobdefinition-ulimit"></a>

The `Ulimit` property type specifies the ulimits to use in a job definition\.

## Syntax<a name="aws-properties-batch-jobdefinition-ulimit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ulimit-syntax.json"></a>

```
{
  "[SoftLimit](#cfn-batch-jobdefinition-ulimit-softlimit)" : Integer,
  "[HardLimit](#cfn-batch-jobdefinition-ulimit-hardlimit)" : Integer,
  "[Name](#cfn-batch-jobdefinition-ulimit-name)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ulimit-syntax.yaml"></a>

```
[SoftLimit](#cfn-batch-jobdefinition-ulimit-softlimit): Integer
[HardLimit](#cfn-batch-jobdefinition-ulimit-hardlimit): Integer
[Name](#cfn-batch-jobdefinition-ulimit-name): String
```

## Properties<a name="aws-properties-batch-jobdefinition-ulimit-properties"></a>

`SoftLimit`  <a name="cfn-batch-jobdefinition-ulimit-softlimit"></a>
The soft limit for the `ulimit` type\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`HardLimit`  <a name="cfn-batch-jobdefinition-ulimit-hardlimit"></a>
The hard limit for the `ulimit` type\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`Name`  <a name="cfn-batch-jobdefinition-ulimit-name"></a>
The `type` of the `ulimit`\.  
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 