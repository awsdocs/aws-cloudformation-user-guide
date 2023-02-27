# AWS::OpenSearchServerless::AccessPolicy<a name="aws-resource-opensearchserverless-accesspolicy"></a>

Creates a data access policy for OpenSearch Serverless\. Access policies limit access to collections and the resources within them, and allow a user to access that data irrespective of the access mechanism or network source\. For more information, see [Data access control for Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-data-access.html)\.

## Syntax<a name="aws-resource-opensearchserverless-accesspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchserverless-accesspolicy-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchServerless::AccessPolicy",
  "Properties" : {
      "[Description](#cfn-opensearchserverless-accesspolicy-description)" : String,
      "[Name](#cfn-opensearchserverless-accesspolicy-name)" : String,
      "[Policy](#cfn-opensearchserverless-accesspolicy-policy)" : String,
      "[Type](#cfn-opensearchserverless-accesspolicy-type)" : String
    }
}
```

### YAML<a name="aws-resource-opensearchserverless-accesspolicy-syntax.yaml"></a>

```
Type: AWS::OpenSearchServerless::AccessPolicy
Properties: 
  [Description](#cfn-opensearchserverless-accesspolicy-description): String
  [Name](#cfn-opensearchserverless-accesspolicy-name): String
  [Policy](#cfn-opensearchserverless-accesspolicy-policy): String
  [Type](#cfn-opensearchserverless-accesspolicy-type): String
```

## Properties<a name="aws-resource-opensearchserverless-accesspolicy-properties"></a>

`Description`  <a name="cfn-opensearchserverless-accesspolicy-description"></a>
The description of the policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opensearchserverless-accesspolicy-name"></a>
The name of the policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-opensearchserverless-accesspolicy-policy"></a>
The JSON policy document without any whitespaces\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opensearchserverless-accesspolicy-type"></a>
The type of access policy\. Currently the only option is `data`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opensearchserverless-accesspolicy-return-values"></a>

### Ref<a name="aws-resource-opensearchserverless-accesspolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the access policy\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-opensearchserverless-accesspolicy--examples"></a>

### Create an access policy that allows access to all collections and indexes<a name="aws-resource-opensearchserverless-accesspolicy--examples--Create_an_access_policy_that_allows_access_to_all_collections_and_indexes"></a>

The following example specifies an OpenSearch Serverless access policy that provides full access to the resources within `my-collection` to the user `test-user`\.

For a complete sample policy that creates network, encryption, and access policies, as well as a matching collection, see [Using AWS CloudFormation to create Amazon OpenSearch Serverless collections](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-cfn.html) in the *Amazon OpenSearch Service Developer Guide\.*

#### JSON<a name="aws-resource-opensearchserverless-accesspolicy--examples--Create_an_access_policy_that_allows_access_to_all_collections_and_indexes--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "OpenSearch Serverless access policy template",
    "Resources": {
        "TestAccessPolicy": {
            "Type": "AWS::OpenSearchServerless::AccessPolicy",
            "Properties": {
                "Name": "test-access-policy",
                "Type": "data",
                "Description": "Access policy for my-collection",
                "Policy": {
                    "Fn::Sub": "[{\"Description\":\"Access for test-user\",\"Rules\":[{\"ResourceType\":\"index\",\"Resource\":[\"index/*/*\"],\"Permission\":[\"aoss:*\"]}, {\"ResourceType\":\"collection\",\"Resource\":[\"collection/my-collection\"],\"Permission\":[\"aoss:*\"]}], \"Principal\":[\"arn:aws:iam::${AWS::AccountId}:user/test-user\"]}]"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-opensearchserverless-accesspolicy--examples--Create_an_access_policy_that_allows_access_to_all_collections_and_indexes--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless access policy template'
Resources:
  TestAccessPolicy:
    Type: 'AWS::OpenSearchServerless::AccessPolicy'
    Properties:
      Name: test-access-policy
      Type: data
      Description: Access policy for my-collection
      Policy: !Sub >-
        [{"Description":"Access for test-user","Rules":[{"ResourceType":"index","Resource":["index/*/*"],"Permission":["aoss:*"]},
        {"ResourceType":"collection","Resource":["collection/my-collection"],"Permission":["aoss:*"]}],
        "Principal":["arn:aws:iam::${AWS::AccountId}:user/test-user"]}]
```