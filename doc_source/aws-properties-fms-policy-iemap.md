# AWS::FMS::Policy IEMap<a name="aws-properties-fms-policy-iemap"></a>

Specifies the AWS account IDs to exclude from or include in the policy\. Used for the policy's `IncludeMap` and `ExcludeMap`\. 

The key to the map is `ACCOUNT`\. For example, a valid `IEMap` would be `{“ACCOUNT” : [“accountID1”, “accountID2”]}`\.

## Syntax<a name="aws-properties-fms-policy-iemap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-iemap-syntax.json"></a>

```
{
  "[ACCOUNT](#cfn-fms-policy-iemap-account)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fms-policy-iemap-syntax.yaml"></a>

```
  [ACCOUNT](#cfn-fms-policy-iemap-account): 
    - String
```

## Properties<a name="aws-properties-fms-policy-iemap-properties"></a>

`ACCOUNT`  <a name="cfn-fms-policy-iemap-account"></a>
The account list for the map\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)