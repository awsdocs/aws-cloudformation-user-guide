# AWS::DynamoDB::Table SSESpecification<a name="aws-properties-dynamodb-table-ssespecification"></a>

Represents the settings used to enable server\-side encryption\.

## Syntax<a name="aws-properties-dynamodb-table-ssespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-ssespecification-syntax.json"></a>

```
{
  "[SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-table-ssespecification-syntax.yaml"></a>

```
﻿  [SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled) : Boolean
```

## Properties<a name="aws-properties-dynamodb-table-ssespecification-properties"></a>

`SSEEnabled`  <a name="cfn-dynamodb-table-ssespecification-sseenabled"></a>
Indicates whether server\-side encryption is enabled \(true\) or disabled \(false\) on the table\. If enabled \(true\), server\-side encryption type is set to `KMS`\. If disabled \(false\) or not specified, server\-side encryption is set to AWS owned CMK\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)