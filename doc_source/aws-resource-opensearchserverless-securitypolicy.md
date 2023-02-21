# AWS::OpenSearchServerless::SecurityPolicy<a name="aws-resource-opensearchserverless-securitypolicy"></a>

Creates an encryption or network policy to be used by one or more OpenSearch Serverless collections\. 

Network policies specify access to a collection and its OpenSearch Dashboards endpoint from public networks or specific VPC endpoints\. For more information, see [Network access for Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-network.html)\.

Encryption policies specify a KMS encryption key to assign to particular collections\. For more information, see [Encryption at rest for Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-encryption.html)\.

## Syntax<a name="aws-resource-opensearchserverless-securitypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchserverless-securitypolicy-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchServerless::SecurityPolicy",
  "Properties" : {
      "[Description](#cfn-opensearchserverless-securitypolicy-description)" : String,
      "[Name](#cfn-opensearchserverless-securitypolicy-name)" : String,
      "[Policy](#cfn-opensearchserverless-securitypolicy-policy)" : String,
      "[Type](#cfn-opensearchserverless-securitypolicy-type)" : String
    }
}
```

### YAML<a name="aws-resource-opensearchserverless-securitypolicy-syntax.yaml"></a>

```
Type: AWS::OpenSearchServerless::SecurityPolicy
Properties: 
  [Description](#cfn-opensearchserverless-securitypolicy-description): String
  [Name](#cfn-opensearchserverless-securitypolicy-name): String
  [Policy](#cfn-opensearchserverless-securitypolicy-policy): String
  [Type](#cfn-opensearchserverless-securitypolicy-type): String
```

## Properties<a name="aws-resource-opensearchserverless-securitypolicy-properties"></a>

`Description`  <a name="cfn-opensearchserverless-securitypolicy-description"></a>
The description of the security policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opensearchserverless-securitypolicy-name"></a>
The name of the policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-opensearchserverless-securitypolicy-policy"></a>
The JSON policy document without any whitespaces\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opensearchserverless-securitypolicy-type"></a>
The type of security policy\. Can be either `encryption` or `network`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opensearchserverless-securitypolicy-return-values"></a>

### Ref<a name="aws-resource-opensearchserverless-securitypolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the security policy\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-opensearchserverless-securitypolicy--examples"></a>

### Create an encryption policy<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_an_encryption_policy"></a>

The following example specifies an OpenSearch Serverless encryption policy named `logs-encryption-policy` with an AWS owned key\. The policy will apply to all future collections with names that begin with "logs"\.

For a complete sample policy that creates network, encryption, and access policies, as well as a matching collection, see [Using AWS CloudFormation to create Amazon OpenSearch Serverless collections](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-cfn.html) in the *Amazon OpenSearch Service Developer Guide\.*

#### JSON<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_an_encryption_policy--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "OpenSearch Serverless encryption policy template",
  "Resources": {
    "TestSecurityPolicy": {
      "Type": "AWS::OpenSearchServerless::SecurityPolicy",
      "Properties": {
        "Name": "logs-encryption-policy",
        "Type": "encryption",
        "Description": "Encryption policy for test collections",
        "Policy": "{\"Rules\":[{\"ResourceType\":\"collection\",\"Resource\":[\"collection/logs*\"]}],\"AWSOwnedKey\":true}"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_an_encryption_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless encryption policy template'
Resources:
  TestSecurityPolicy:
    Type: 'AWS::OpenSearchServerless::SecurityPolicy'
    Properties:
      Name: logs-encryption-policy
      Type: encryption
      Description: Encryption policy for test collections
      Policy: >-
        {"Rules":[{"ResourceType":"collection","Resource":["collection/logs*"]}],"AWSOwnedKey":true}
```

### Create a network policy<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_a_network_policy"></a>

The following example specifies an OpenSearch Serverless network policy named `logs-network-policy`\. It provides public access to OpenSearch endpoints and OpenSearch Dashboards endpoints\. The policy will apply to all collections with names that begin with "logs"\.

#### JSON<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_a_network_policy--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Description":"OpenSearch Serverless network policy template",
   "Resources":{
      "SecurityPolicy":{
         "Type":"AWS::OpenSearchServerless::SecurityPolicy",
         "Properties":{
            "Name":"logs-network-policy",
            "Type":"network",
            "Description":"Network policy for test collections",
            "Policy":"[{\"Rules\":[{\"ResourceType\":\"collection\",\"Resource\":[\"collection/logs*\"]}, {\"ResourceType\":\"dashboard\",\"Resource\":[\"collection/logs*\"]}],\"AllowFromPublic\":true}]"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-opensearchserverless-securitypolicy--examples--Create_a_network_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless network policy template'
Resources:
  SecurityPolicy:
    Type: 'AWS::OpenSearchServerless::SecurityPolicy'
    Properties:
      Name: logs-network-policy
      Type: network
      Description: Network policy for test collections
      Policy: >-
        [{"Rules":[{"ResourceType":"collection","Resource":["collection/logs*"]}, {"ResourceType":"dashboard","Resource":["collection/logs*"]}],"AllowFromPublic":true}]
```