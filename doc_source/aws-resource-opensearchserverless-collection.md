# AWS::OpenSearchServerless::Collection<a name="aws-resource-opensearchserverless-collection"></a>

Specifies an OpenSearch Serverless collection\. For more information, see [Creating and managing Amazon OpenSearch Serverless collections](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-manage.html) in the *Amazon OpenSearch Service Developer Guide*\.

**Important**  
You must create a matching [encryption policy](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-encryption.html) in order for a collection to be created successfully\. You can specify the policy resource within the same CloudFormation template as the collection resource if you use the [DependsOn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) attribute\. See [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-collection.html#aws-resource-opensearchserverless-collection--examples) for a sample template\. Otherwise the encryption policy must already exist before you create the collection\.

## Syntax<a name="aws-resource-opensearchserverless-collection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchserverless-collection-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchServerless::Collection",
  "Properties" : {
      "[Description](#cfn-opensearchserverless-collection-description)" : String,
      "[Name](#cfn-opensearchserverless-collection-name)" : String,
      "[Tags](#cfn-opensearchserverless-collection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-opensearchserverless-collection-type)" : String
    }
}
```

### YAML<a name="aws-resource-opensearchserverless-collection-syntax.yaml"></a>

```
Type: AWS::OpenSearchServerless::Collection
Properties: 
  [Description](#cfn-opensearchserverless-collection-description): String
  [Name](#cfn-opensearchserverless-collection-name): String
  [Tags](#cfn-opensearchserverless-collection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-opensearchserverless-collection-type): String
```

## Properties<a name="aws-resource-opensearchserverless-collection-properties"></a>

`Description`  <a name="cfn-opensearchserverless-collection-description"></a>
A description of the collection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opensearchserverless-collection-name"></a>
The name of the collection\.  
Collection names must meet the following criteria:  
+ Starts with a lowercase letter
+ Unique to your account and AWS Region
+ Contains between 3 and 28 characters
+ Contains only lowercase letters a\-z, the numbers 0\-9, and the hyphen \(\-\)
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-opensearchserverless-collection-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with the collection\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-opensearchserverless-collection-type"></a>
The type of collection\. Possible values are `SEARCH` and `TIMESERIES`\. For more information, see [Choosing a collection type](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-overview.html#serverless-usecase)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opensearchserverless-collection-return-values"></a>

### Ref<a name="aws-resource-opensearchserverless-collection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the collection ID\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opensearchserverless-collection-return-values-fn--getatt"></a>

`GetAtt` returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-opensearchserverless-collection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the collection\. For example, `arn:aws:aoss:us-east-1:123456789012:collection/07tjusf2h91cunochc`\.

`CollectionEndpoint`  <a name="CollectionEndpoint-fn::getatt"></a>
Collection\-specific endpoint used to submit index, search, and data upload requests to an OpenSearch Serverless collection\. For example, `https://07tjusf2h91cunochc.us-east-1.aoss.amazonaws.com`\.

`DashboardEndpoint`  <a name="DashboardEndpoint-fn::getatt"></a>
Collection\-specific endpoint used to access OpenSearch Dashboards\. For example, `https://07tjusf2h91cunochc.us-east-1.aoss.amazonaws.com/_dashboards`\.

`Id`  <a name="Id-fn::getatt"></a>
A unique identifier for the collection\. For example, `07tjusf2h91cunochc`\.

## Examples<a name="aws-resource-opensearchserverless-collection--examples"></a>

### Create a collection<a name="aws-resource-opensearchserverless-collection--examples--Create_a_collection"></a>

The following example specifies an OpenSearch Serverless collection named `test-collection`\. The collection type is `SEARCH`\. The template also creates a matching encryption policy, which is required in order for the collection to be created successfully\.

For a complete sample policy that creates network, encryption, and access policies, as well as a matching collection, see [Using AWS CloudFormation to create Amazon OpenSearch Serverless collections](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-cfn.html) in the *Amazon OpenSearch Service Developer Guide\.*

**Note**  
This example uses public network access, which isn't recommended for production workloads\. We recommend using VPC access to protect your collections\. For more information, see [AWS::OpenSearchServerless::VpcEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-vpcendpoint.html) and [Access Amazon OpenSearch Serverless using an interface endpoint](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-vpc.html)\.

#### JSON<a name="aws-resource-opensearchserverless-collection--examples--Create_a_collection--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "OpenSearch Serverless collection template",
    "Resources": {
        "TestCollection": {
            "Type": "AWS::OpenSearchServerless::Collection",
            "Properties": {
                "Name": "test-collection",
                "Type": "SEARCH",
                "Description": "Search collection"
            },
            "DependsOn": "EncryptionPolicy"
        },
        "EncryptionPolicy": {
            "Type": "AWS::OpenSearchServerless::SecurityPolicy",
            "Properties": {
                "Name": "test-encryption-policy",
                "Type": "encryption",
                "Description": "Encryption policy for test collection",
                "Policy": "{\"Rules\":[{\"ResourceType\":\"collection\",\"Resource\":[\"collection/test-collection\"]}],\"AWSOwnedKey\":true}"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-opensearchserverless-collection--examples--Create_a_collection--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless collection template'
Resources:
  TestCollection:
    Type: 'AWS::OpenSearchServerless::Collection'
    Properties:
      Name: test-collection
      Type: SEARCH
      Description: Search collection
    DependsOn: EncryptionPolicy
  EncryptionPolicy:
    Type: 'AWS::OpenSearchServerless::SecurityPolicy'
    Properties:
      Name: test-encryption-policy
      Type: encryption
      Description: Encryption policy for test collection
      Policy: >-
        {"Rules":[{"ResourceType":"collection","Resource":["collection/test-collection"]}],"AWSOwnedKey":true}
```