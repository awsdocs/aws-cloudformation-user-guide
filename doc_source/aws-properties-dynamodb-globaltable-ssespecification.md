# AWS::DynamoDB::GlobalTable SSESpecification<a name="aws-properties-dynamodb-globaltable-ssespecification"></a>

Represents the settings used to enable server\-side encryption\.

## Syntax<a name="aws-properties-dynamodb-globaltable-ssespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-ssespecification-syntax.json"></a>

```
{
  "[SSEEnabled](#cfn-dynamodb-globaltable-ssespecification-sseenabled)" : Boolean,
  "[SSEType](#cfn-dynamodb-globaltable-ssespecification-ssetype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-ssespecification-syntax.yaml"></a>

```
  [SSEEnabled](#cfn-dynamodb-globaltable-ssespecification-sseenabled): Boolean
  [SSEType](#cfn-dynamodb-globaltable-ssespecification-ssetype): String
```

## Properties<a name="aws-properties-dynamodb-globaltable-ssespecification-properties"></a>

`SSEEnabled`  <a name="cfn-dynamodb-globaltable-ssespecification-sseenabled"></a>
Indicates whether server\-side encryption is performed using an AWS managed key or an AWS owned key\. If enabled \(true\), server\-side encryption type is set to KMS and an AWS managed key is used \(AWS KMS charges apply\)\. If disabled \(false\) or not specified,server\-side encryption is set to an AWS owned key\. If you choose to use KMS encryption, you can also use customer managed KMS keys by specifying them in the `ReplicaSpecification.SSESpecification` object\. You cannot mix AWS managed and customer managed KMS keys\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSEType`  <a name="cfn-dynamodb-globaltable-ssespecification-ssetype"></a>
Server\-side encryption type\. The only supported value is:  
+  `KMS` \- Server\-side encryption that uses AWS Key Management Service\. The key is stored in your account and is managed by AWS KMS \(AWS KMS charges apply\)\.
*Required*: No  
*Type*: String  
*Allowed values*: `AES256 | KMS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)