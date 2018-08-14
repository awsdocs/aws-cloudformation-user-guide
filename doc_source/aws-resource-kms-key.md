# AWS::KMS::Key<a name="aws-resource-kms-key"></a>

The `AWS::KMS::Key` resource creates a customer master key \(CMK\) in AWS Key Management Service \(AWS KMS\)\. Users \(customers\) can use the master key to encrypt their data stored in AWS services that are integrated with AWS KMS or within their applications\. For more information, see [What is the AWS Key Management Service?](http://docs.aws.amazon.com/kms/latest/developerguide/) in the *AWS Key Management Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-kms-key-syntax)
+ [Properties](#w3ab2c21c10d843b9)
+ [Return Values](#w3ab2c21c10d843c11)
+ [Examples](#w3ab2c21c10d843c13)

## Syntax<a name="aws-resource-kms-key-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kms-key-syntax.json"></a>

```
{
  "Type" : "AWS::KMS::Key",
  "Properties" : {
    "[Description](#cfn-kms-key-description)" : String,
    "[Enabled](#cfn-kms-key-enabled)" : Boolean,
    "[EnableKeyRotation](#cfn-kms-key-enablekeyrotation)" : Boolean,
    "[KeyPolicy](#cfn-kms-key-keypolicy)" : JSON object
    "[Tags](#cfn-kms-key-tags)" : [ Resource Tag, ... ],
  }
}
```

### YAML<a name="aws-resource-kms-key-syntax.yaml"></a>

```
Type: "AWS::KMS::Key"
Properties: 
  [Description](#cfn-kms-key-description): String
  [Enabled](#cfn-kms-key-enabled): Boolean
  [EnableKeyRotation](#cfn-kms-key-enablekeyrotation): Boolean
  [KeyPolicy](#cfn-kms-key-keypolicy): JSON object
  [Tags](#cfn-kms-key-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d843b9"></a>

`Description`  <a name="cfn-kms-key-description"></a>
A description of the key\. Use a description that helps your users decide whether the key is appropriate for a particular task\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Enabled`  <a name="cfn-kms-key-enabled"></a>
Indicates whether the key is available for use\. AWS CloudFormation sets this value to `true` by default\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EnableKeyRotation`  <a name="cfn-kms-key-enablekeyrotation"></a>
Indicates whether AWS KMS rotates the key\. AWS CloudFormation sets this value to `false` by default\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KeyPolicy`  <a name="cfn-kms-key-keypolicy"></a>
An AWS KMS key policy to attach to the key\. Use a policy to specify who has permission to use the key and which actions they can perform\. For more information, see [Key Policies](http://docs.aws.amazon.com/kms/latest/developerguide/key-policies.html) in the *AWS Key Management Service Developer Guide*\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-kms-key-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this key\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d843c11"></a>

### Ref<a name="w3ab2c21c10d843c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, it returns the key ID, such as `123ab456-a4c2-44cb-95fd-b781f32fbb37`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d843c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The ARN of the AWS KMS key, such as `arn:aws:kms:us-west-2:123456789012:key/12a34567-8c90-1defg-af84-0bf06c1747f3`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d843c13"></a>

### <a name="w3ab2c21c10d843c13b2"></a>

The following example creates a custom CMK, which permits the IAM user `Alice` to administer the key and allows `Bob` to use the key for encrypting and decrypting data\.

#### JSON<a name="aws-resource-kms-key-example.json"></a>

```
"myKey" : {
  "Type" : "AWS::KMS::Key",
  "Properties" : {
    "Description" : "A sample key",
    "KeyPolicy" : {
      "Version": "2012-10-17",
      "Id": "key-default-1",
      "Statement": [
        {
          "Sid": "Allow administration of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::123456789012:user/Alice" },
          "Action": [
            "kms:Create*",
            "kms:Describe*",
            "kms:Enable*",
            "kms:List*",
            "kms:Put*",
            "kms:Update*",
            "kms:Revoke*",
            "kms:Disable*",
            "kms:Get*",
            "kms:Delete*",
            "kms:ScheduleKeyDeletion",
            "kms:CancelKeyDeletion"
          ],
          "Resource": "*"
        },
        {
          "Sid": "Allow use of the key",
          "Effect": "Allow",
          "Principal": { "AWS": "arn:aws:iam::123456789012:user/Bob" },
          "Action": [
            "kms:Encrypt",
            "kms:Decrypt",
            "kms:ReEncrypt*",
            "kms:GenerateDataKey*",
            "kms:DescribeKey"
          ], 
          "Resource": "*"
        }    
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key-example.yaml"></a>

```
myKey: 
  Type: "AWS::KMS::Key"
  Properties: 
    Description: "A sample key"
    KeyPolicy: 
      Version: "2012-10-17"
      Id: "key-default-1"
      Statement: 
        - 
          Sid: "Allow administration of the key"
          Effect: "Allow"
          Principal: 
            AWS: "arn:aws:iam::123456789012:user/Alice"
          Action: 
            - "kms:Create*"
            - "kms:Describe*"
            - "kms:Enable*"
            - "kms:List*"
            - "kms:Put*"
            - "kms:Update*"
            - "kms:Revoke*"
            - "kms:Disable*"
            - "kms:Get*"
            - "kms:Delete*"
            - "kms:ScheduleKeyDeletion"
            - "kms:CancelKeyDeletion"
          Resource: "*"
        - 
          Sid: "Allow use of the key"
          Effect: "Allow"
          Principal: 
            AWS: "arn:aws:iam::123456789012:user/Bob"
          Action: 
            - "kms:Encrypt"
            - "kms:Decrypt"
            - "kms:ReEncrypt*"
            - "kms:GenerateDataKey*"
            - "kms:DescribeKey"
          Resource: "*"
```

### <a name="aws-resource-kms-key-example-tags"></a>

The following example creates a custom CMK with a single tag\.

#### JSON<a name="aws-resource-kms-key-example-tags.json"></a>

```
{
  "Resources" : {
    "myKey" : {
      "Type" : "AWS::KMS::Key",
      "Properties" : {
        "KeyPolicy" : {
          "Version": "2012-10-17",
          "Id": "key-default-1",
          "Statement": [
            {
              "Sid": "Enable IAM User Permissions",
              "Effect": "Allow",
              "Principal": {
                "AWS": { "Fn::Join" : ["" , ["arn:aws:iam::", {"Ref" : "AWS::AccountId"} ,":root" ]] }
              },
              "Action": "kms:*",
              "Resource": "*"
            }
          ]
        },
        "Tags" : [
          {
            "Key" : {"Ref" : "Key"},
            "Value" : {"Ref" : "Value"}
          }
        ]
      }
    }
  },
  "Parameters" : {
    "Key" : {
      "Type" : "String"
    },
    "Value" : {
      "Type" : "String"
    }
  }
}
```

#### YAML<a name="aws-resource-kms-key-example-tags.yaml"></a>

```
Resources:
  myKey:
    Type: 'AWS::KMS::Key'
    Properties:
      KeyPolicy:
        Version: 2012-10-17
        Id: key-default-1
        Statement:
          - Sid: Enable IAM User Permissions
            Effect: Allow
            Principal:
              AWS: !Join 
                - ''
                - - 'arn:aws:iam::'
                  - !Ref 'AWS::AccountId'
                  - ':root'
            Action: 'kms:*'
            Resource: '*'
      Tags:
        - Key: !Ref Key
          Value: !Ref Value
Parameters:
  Key:
    Type: String
  Value:
    Type: String
```