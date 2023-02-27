# AWS::Transfer::Agreement<a name="aws-resource-transfer-agreement"></a>

Creates an agreement\. An agreement is a bilateral trading partner agreement, or partnership, between an AWS Transfer Family server and an AS2 process\. The agreement defines the file and message transfer relationship between the server and the AS2 process\. To define an agreement, Transfer Family combines a server, local profile, partner profile, certificate, and other attributes\.

The partner is identified with the `PartnerProfileId`, and the AS2 process is identified with the `LocalProfileId`\.

## Syntax<a name="aws-resource-transfer-agreement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-agreement-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Agreement",
  "Properties" : {
      "[AccessRole](#cfn-transfer-agreement-accessrole)" : String,
      "[BaseDirectory](#cfn-transfer-agreement-basedirectory)" : String,
      "[Description](#cfn-transfer-agreement-description)" : String,
      "[LocalProfileId](#cfn-transfer-agreement-localprofileid)" : String,
      "[PartnerProfileId](#cfn-transfer-agreement-partnerprofileid)" : String,
      "[ServerId](#cfn-transfer-agreement-serverid)" : String,
      "[Status](#cfn-transfer-agreement-status)" : String,
      "[Tags](#cfn-transfer-agreement-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-transfer-agreement-syntax.yaml"></a>

```
Type: AWS::Transfer::Agreement
Properties: 
  [AccessRole](#cfn-transfer-agreement-accessrole): String
  [BaseDirectory](#cfn-transfer-agreement-basedirectory): String
  [Description](#cfn-transfer-agreement-description): String
  [LocalProfileId](#cfn-transfer-agreement-localprofileid): String
  [PartnerProfileId](#cfn-transfer-agreement-partnerprofileid): String
  [ServerId](#cfn-transfer-agreement-serverid): String
  [Status](#cfn-transfer-agreement-status): String
  [Tags](#cfn-transfer-agreement-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-transfer-agreement-properties"></a>

`AccessRole`  <a name="cfn-transfer-agreement-accessrole"></a>
With AS2, you can send files by calling `StartFileTransfer` and specifying the file paths in the request parameter, `SendFilePaths`\. We use the file’s parent directory \(for example, for `--send-file-paths /bucket/dir/file.txt`, parent directory is `/bucket/dir/`\) to temporarily store a processed AS2 message file, store the MDN when we receive them from the partner, and write a final JSON file containing relevant metadata of the transmission\. So, the `AccessRole` needs to provide read and write access to the parent directory of the file location used in the `StartFileTransfer` request\. Additionally, you need to provide read and write access to the parent directory of the files that you intend to send with `StartFileTransfer`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseDirectory`  <a name="cfn-transfer-agreement-basedirectory"></a>
The landing directory \(folder\) for files that are transferred by using the AS2 protocol\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^$|/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-transfer-agreement-description"></a>
The name or short description that's used to identify the agreement\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^[\p{Graph}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalProfileId`  <a name="cfn-transfer-agreement-localprofileid"></a>
A unique identifier for the AS2 local profile\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `19`  
*Maximum*: `19`  
*Pattern*: `^p-([0-9a-f]{17})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PartnerProfileId`  <a name="cfn-transfer-agreement-partnerprofileid"></a>
A unique identifier for the partner profile used in the agreement\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `19`  
*Maximum*: `19`  
*Pattern*: `^p-([0-9a-f]{17})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerId`  <a name="cfn-transfer-agreement-serverid"></a>
A system\-assigned unique identifier for a server instance\. This identifier indicates the specific server that the agreement uses\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `19`  
*Maximum*: `19`  
*Pattern*: `^s-([0-9a-f]{17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-transfer-agreement-status"></a>
The current status of the agreement, either `ACTIVE` or `INACTIVE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTIVE | INACTIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-transfer-agreement-tags"></a>
Key\-value pairs that can be used to group and search for agreements\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-agreement-return-values"></a>

### Ref<a name="aws-resource-transfer-agreement-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-transfer-agreement-return-values-fn--getatt"></a>

#### <a name="aws-resource-transfer-agreement-return-values-fn--getatt-fn--getatt"></a>

`AgreementId`  <a name="AgreementId-fn::getatt"></a>
Property description not available\.

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.