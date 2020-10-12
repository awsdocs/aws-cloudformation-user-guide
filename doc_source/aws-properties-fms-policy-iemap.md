# AWS::FMS::Policy IEMap<a name="aws-properties-fms-policy-iemap"></a>

Specifies the AWS account IDs and AWS Organizations organizational units \(OUs\) to include in or exclude from the policy\. Specifying an OU is the equivalent of specifying all accounts in the OU and in any of its child OUs, including any child OUs and accounts that are added at a later time\.

This is used for the policy's `IncludeMap` and `ExcludeMap`\.

You can specify account IDs, OUs, or a combination: 
+ Specify account IDs by setting the key to `ACCOUNT`\. For example, the following is a valid map: `{“ACCOUNT” : [“accountID1”, “accountID2”]}`\.
+ Specify OUs by setting the key to `ORGUNIT`\. For example, the following is a valid map: `{“ORGUNIT” : [“ouid111”, “ouid112”]}`\.
+ Specify accounts and OUs together in a single map, separated with a comma\. For example, the following is a valid map: `{“ACCOUNT” : [“accountID1”, “accountID2”], “ORGUNIT” : [“ouid111”, “ouid112”]}`\.

## Syntax<a name="aws-properties-fms-policy-iemap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-iemap-syntax.json"></a>

```
{
  "[ACCOUNT](#cfn-fms-policy-iemap-account)" : [ String, ... ],
  "[ORGUNIT](#cfn-fms-policy-iemap-orgunit)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fms-policy-iemap-syntax.yaml"></a>

```
  [ACCOUNT](#cfn-fms-policy-iemap-account): 
    - String
  [ORGUNIT](#cfn-fms-policy-iemap-orgunit): 
    - String
```

## Properties<a name="aws-properties-fms-policy-iemap-properties"></a>

`ACCOUNT`  <a name="cfn-fms-policy-iemap-account"></a>
The account list for the map\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ORGUNIT`  <a name="cfn-fms-policy-iemap-orgunit"></a>
The organizational unit list for the map\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)