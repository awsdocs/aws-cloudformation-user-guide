# AWS::Route53::KeySigningKey<a name="aws-resource-route53-keysigningkey"></a>

The `AWS::Route53::KeySigningKey` resource creates a new key\-signing key \(KSK\) in a hosted zone\. The hosted zone ID is passed as a parameter in the KSK properties\. You can specify the properties of this KSK using the `Name`, `Status`, and `KeyManagementServiceArn `properties of the resource\.

## Syntax<a name="aws-resource-route53-keysigningkey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-keysigningkey-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::KeySigningKey",
  "Properties" : {
      "[HostedZoneId](#cfn-route53-keysigningkey-hostedzoneid)" : String,
      "[KeyManagementServiceArn](#cfn-route53-keysigningkey-keymanagementservicearn)" : String,
      "[Name](#cfn-route53-keysigningkey-name)" : String,
      "[Status](#cfn-route53-keysigningkey-status)" : String
    }
}
```

### YAML<a name="aws-resource-route53-keysigningkey-syntax.yaml"></a>

```
Type: AWS::Route53::KeySigningKey
Properties: 
  [HostedZoneId](#cfn-route53-keysigningkey-hostedzoneid): String
  [KeyManagementServiceArn](#cfn-route53-keysigningkey-keymanagementservicearn): String
  [Name](#cfn-route53-keysigningkey-name): String
  [Status](#cfn-route53-keysigningkey-status): String
```

## Properties<a name="aws-resource-route53-keysigningkey-properties"></a>

`HostedZoneId`  <a name="cfn-route53-keysigningkey-hostedzoneid"></a>
The unique string \(ID\) that is used to identify a hosted zone\. For example: `Z00001111A1ABCaaABC11`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyManagementServiceArn`  <a name="cfn-route53-keysigningkey-keymanagementservicearn"></a>
The Amazon resource name \(ARN\) for a customer managed customer master key \(CMK\) in AWS Key Management Service \(AWS KMS \)\. The `KeyManagementServiceArn` must be unique for each key\-signing key \(KSK\) in a single hosted zone\. For example: `arn:aws:kms:us-east-1:111122223333:key/111a2222-a11b-1ab1-2ab2-1ab21a2b3a111`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-route53-keysigningkey-name"></a>
A string used to identify a key\-signing key \(KSK\)\. `Name` can include numbers, letters, and underscores \(\_\)\. `Name` must be unique for each key\-signing key in the same hosted zone\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-route53-keysigningkey-status"></a>
A string that represents the current key\-signing key \(KSK\) status\.  
Status can have one of the following values:    
ACTIVE  
The KSK is being used for signing\.  
INACTIVE  
The KSK is not being used for signing\.  
DELETING  
The KSK is in the process of being deleted\.  
ACTION\_NEEDED  
There is a problem with the KSK that requires you to take action to resolve\. For example, the customer managed key might have been deleted, or the permissions for the customer managed key might have been changed\.  
INTERNAL\_FAILURE  
There was an error during a request\. Before you can continue to work with DNSSEC signing, including actions that involve this KSK, you must correct the problem\. For example, you may need to activate or deactivate the KSK\.
*Required*: Yes  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `150`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53-keysigningkey-return-values"></a>

### Ref<a name="aws-resource-route53-keysigningkey-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a identifier that is based on both the hosted zone ID and the KSK name properties\. For example:

 `{ "Ref": "Z00001111A1ABCaaABC11|KSK1" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.