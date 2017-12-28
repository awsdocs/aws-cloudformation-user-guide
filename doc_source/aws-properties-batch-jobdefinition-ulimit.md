# AWS Batch JobDefinition Ulimit<a name="aws-properties-batch-jobdefinition-ulimit"></a>

The `Ulimit` property type specifies the ulimits to use in a job definition\.

## Syntax<a name="aws-properties-batch-jobdefinition-ulimit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ulimit-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-softlimit)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-hardlimit)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-name)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ulimit-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-softlimit): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-hardlimit): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-ulimit-name): String
```

## Properties<a name="aws-properties-batch-jobdefinition-ulimit-properties"></a>

`SoftLimit`  
The soft limit for the `ulimit` type\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`HardLimit`  
The hard limit for the `ulimit` type\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`Name`  
The `type` of the `ulimit`\.  
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 