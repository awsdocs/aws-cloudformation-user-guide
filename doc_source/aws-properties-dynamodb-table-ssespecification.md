# AWS::DynamoDB::Table SSESpecification<a name="aws-properties-dynamodb-table-ssespecification"></a>

Represents the settings used to enable server\-side encryption\.

## Syntax<a name="aws-properties-dynamodb-table-ssespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-ssespecification-syntax.json"></a>

```
{
  "[KMSMasterKeyId](#cfn-dynamodb-table-ssespecification-kmsmasterkeyid)" : String,
  "[SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled)" : Boolean,
  "[SSEType](#cfn-dynamodb-table-ssespecification-ssetype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-table-ssespecification-syntax.yaml"></a>

```
  [KMSMasterKeyId](#cfn-dynamodb-table-ssespecification-kmsmasterkeyid): String
  [SSEEnabled](#cfn-dynamodb-table-ssespecification-sseenabled): Boolean
  [SSEType](#cfn-dynamodb-table-ssespecification-ssetype): String
```

## Properties<a name="aws-properties-dynamodb-table-ssespecification-properties"></a>

`KMSMasterKeyId`  <a name="cfn-dynamodb-table-ssespecification-kmsmasterkeyid"></a>
The AWS KMS customer master key \(CMK\) that should be used for the AWS KMS encryption\. To specify a CMK, use its key ID, Amazon Resource Name \(ARN\), alias name, or alias ARN\. Note that you should only provide this parameter if the key is different from the default DynamoDB customer master key alias/aws/dynamodb\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSEEnabled`  <a name="cfn-dynamodb-table-ssespecification-sseenabled"></a>
Indicates whether server\-side encryption is done using an AWS managed CMK or an AWS owned CMK\. If enabled \(true\), server\-side encryption type is set to `KMS` and an AWS managed CMK is used \(AWS KMS charges apply\)\. If disabled \(false\) or not specified, server\-side encryption is set to AWS owned CMK\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSEType`  <a name="cfn-dynamodb-table-ssespecification-ssetype"></a>
Server\-side encryption type\. The only supported value is:  
+  `KMS` \- Server\-side encryption that uses AWS Key Management Service\. The key is stored in your account and is managed by AWS KMS \(AWS KMS charges apply\)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)