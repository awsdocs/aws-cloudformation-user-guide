# Intrinsic function references in DeletionPolicy and UpdateReplacePolicy attributes<a name="function-refs-in-policy-attributes"></a>

When you add the `AWS::LanguageExtensions` transform in a AWS CloudFormation template, you can use intrinsic functions to define the `DeletionPolicy` and `UpdateReplacePolicy` resource attributes\.

**Note**  
The intrinsic function must resolve to valid [`DeletionPolicy` options](aws-attribute-deletionpolicy.md) or [`UpdateReplacePolicy` options](aws-attribute-updatereplacepolicy.md)\.

## Declaration<a name="function-refs-in-policy-attributes-declaration"></a>

### JSON<a name="function-refs-in-policy-attributes-syntax.json"></a>

```
{ "DeletionPolicy": IntrinsicFunction }
```

```
{ "UpdateReplacePolicy": IntrinsicFunction }
```

### YAML<a name="function-refs-in-policy-attributes-syntax.yaml"></a>

```
DeletionPolicy: IntrinsicFunction
```

```
UpdateReplacePolicy: IntrinsicFunction
```

## Parameters<a name="function-refs-in-policy-attributes-parameters"></a>

`IntrinsicFunction`  
The intrinsic function that resolves to a valid DeletionPolicy or UpdateReplacePolicy option\.

## Examples<a name="function-refs-in-policy-attributes-examples"></a>

### Define the DeletionPolicy and UpdateReplacePolicy using the Fn:If intrinsic function<a name="function-refs-in-policy-attributes-example1"></a>

The following example sets the `DeletionPolicy` and `UpdateReplacePolicy` attributes based on the condition defined in the `Fn::If` intrinsic function\. If the `Stage` parameter is `Prod`, the `DeletionPolicy` and `UpdateReplacePolicy` attributes will be set to `Retain`\.

#### JSON<a name="function-refs-in-policy-attributes-example1.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion": "2010-09-09",
 3.     "Transform": "AWS::LanguageExtensions",
 4.     "Parameters": {
 5.         "Stage": {
 6.             "Type": "String",
 7.             "AllowedValues": [
 8.                 "Prod",
 9.                 "Staging",
10.                 "Dev"
11.             ]
12.         }
13.     },
14.     "Conditions": {
15.         "IsProd": {
16.             "Fn::Equals": [
17.                 {
18.                     "Ref": "Stage"
19.                 },
20.                 "Prod"
21.             ]
22.         }
23.     },
24.     "Resources": {
25.         "Table": {
26.             "Type": "AWS::DynamoDB::Table",
27.             "Properties": {
28.                 "KeySchema": [{
29.                     "AttributeName": "primaryKey",
30.                     "KeyType": "HASH"
31.                 }],
32.                 "AttributeDefinitions": [{
33.                         "AttributeName": "primaryKey",
34.                         "AttributeType": "S"
35.                 }]
36.             },
37.             "DeletionPolicy": {
38.                 "Fn::If": [
39.                     "IsProd",
40.                     "Retain",
41.                     "Delete"
42.                 ]
43.             },
44.             "UpdateReplacePolicy": {
45.                 "Fn::If": [
46.                     "IsProd",
47.                     "Retain",
48.                     "Delete"
49.                 ]
50.             }
51.         }
52.     }
53. }
```

#### YAML<a name="function-refs-in-policy-attributes-example1.yaml"></a>

```
 1. AWSTemplateFormatVersion: 2010-09-09
 2. Transform: 'AWS::LanguageExtensions'
 3. Parameters:
 4.   Stage:
 5.     Type: String
 6.     AllowedValues:
 7.       - Prod
 8.       - Staging
 9.       - Dev
10. Conditions:
11.   IsProd: !Equals 
12.     - !Ref Stage
13.     - Prod
14. Resources:
15.   Table:
16.     Type: 'AWS::DynamoDB::Table'
17.     Properties:
18.       KeySchema:
19.         - AttributeName: primaryKey
20.           KeyType: HASH
21.       AttributeDefinitions:
22.         - AttributeName: primaryKey
23.           AttributeType: S
24.     DeletionPolicy: !If 
25.       - IsProd
26.       - Retain
27.       - Delete
28.     UpdateReplacePolicy: !If 
29.       - IsProd
30.       - Retain
31.       - Delete
```

### Define the DeletionPolicy and UpdateReplacePolicy attributes using the Ref intrinsic function<a name="function-refs-in-policy-attributes-example2"></a>

The following example sets the `DeletionPolicy` and `UpdateReplacePolicy` attributes based on the value resolved by the `Ref` intrinsic function\. If the `DeletionPolicyParam` and `UpdateReplacePolicyParam` parameters are both set to `Retain`, the `DeletionPolicy` and `UpdateReplacePolicy` attributes are also set to `Retain`\.

#### JSON<a name="function-refs-in-policy-attributes-example2.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion": "2010-09-09",
 3.     "Transform": "AWS::LanguageExtensions",
 4.     "Parameters": {
 5.         "DeletionPolicyParam": {
 6.             "Type": "String",
 7.             "AllowedValues": [
 8.                 "Delete",
 9.                 "Retain",
10.                 "Snapshot"
11.             ],
12.             "Default": "Delete"
13.         },
14.         "UpdateReplacePolicyParam": {
15.             "Type": "String",
16.             "AllowedValues": [
17.                 "Delete",
18.                 "Retain",
19.                 "Snapshot"
20.             ],
21.             "Default": "Delete"
22.         }
23.     },
24.     "Resources": {
25.         "Table": {
26.             "Type": "AWS::DynamoDB::Table",
27.             "Properties": {
28.                 "KeySchema": [
29.                     {
30.                         "AttributeName": "primaryKey",
31.                         "KeyType": "HASH"
32.                 }],
33.                 "AttributeDefinitions": [{
34.                     "AttributeName": "primaryKey",
35.                     "AttributeType": "S"
36.                 }]
37.             },
38.             "DeletionPolicy": {
39.                 "Ref": "DeletionPolicyParam"
40.             },
41.             "UpdateReplacePolicy": {
42.                 "Ref": "UpdateReplacePolicyParam"
43.             }
44.         }
45.     }
46. }
```

#### YAML<a name="function-refs-in-policy-attributes-example2.yaml"></a>

```
 1. AWSTemplateFormatVersion: 2010-09-09
 2. Transform: 'AWS::LanguageExtensions'
 3. Parameters:
 4.   DeletionPolicyParam:
 5.     Type: String
 6.     AllowedValues:
 7.       - Delete
 8.       - Retain
 9.       - Snapshot
10.     Default: Delete
11.   UpdateReplacePolicyParam:
12.     Type: String
13.     AllowedValues:
14.       - Delete
15.       - Retain
16.       - Snapshot
17.     Default: Delete
18. Resources:
19.   Table:
20.     Type: 'AWS::DynamoDB::Table'
21.     Properties:
22.       KeySchema:
23.         - AttributeName: primaryKey
24.           KeyType: HASH
25.       AttributeDefinitions:
26.         - AttributeName: primaryKey
27.           AttributeType: S
28.     DeletionPolicy: !Ref DeletionPolicyParam
29.     UpdateReplacePolicy: !Ref UpdateReplacePolicyParam
```

## Supported functions<a name="function-refs-in-policy-attributes-supported-functions"></a>

Within the `DeletionPolicy` or `UpdateReplacePolicy` attributes, you can use the following functions:
+ `Fn::FindInMap`
+ `Fn::If`
+ `Ref`

You can also use the following [Pseudo parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html):
+ `AWS::AccountId`
+ `AWS::Partition`
+ `AWS::Region`