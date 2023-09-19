# AWS::MediaPackageV2::OriginEndpoint SpekeKeyProvider<a name="aws-properties-mediapackagev2-originendpoint-spekekeyprovider"></a>

The parameters for the SPEKE key provider\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-spekekeyprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-spekekeyprovider-syntax.json"></a>

```
{
  "[DrmSystems](#cfn-mediapackagev2-originendpoint-spekekeyprovider-drmsystems)" : [ String, ... ],
  "[EncryptionContractConfiguration](#cfn-mediapackagev2-originendpoint-spekekeyprovider-encryptioncontractconfiguration)" : EncryptionContractConfiguration,
  "[ResourceId](#cfn-mediapackagev2-originendpoint-spekekeyprovider-resourceid)" : String,
  "[RoleArn](#cfn-mediapackagev2-originendpoint-spekekeyprovider-rolearn)" : String,
  "[Url](#cfn-mediapackagev2-originendpoint-spekekeyprovider-url)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-spekekeyprovider-syntax.yaml"></a>

```
  [DrmSystems](#cfn-mediapackagev2-originendpoint-spekekeyprovider-drmsystems): 
    - String
  [EncryptionContractConfiguration](#cfn-mediapackagev2-originendpoint-spekekeyprovider-encryptioncontractconfiguration): 
    EncryptionContractConfiguration
  [ResourceId](#cfn-mediapackagev2-originendpoint-spekekeyprovider-resourceid): String
  [RoleArn](#cfn-mediapackagev2-originendpoint-spekekeyprovider-rolearn): String
  [Url](#cfn-mediapackagev2-originendpoint-spekekeyprovider-url): String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-spekekeyprovider-properties"></a>

`DrmSystems`  <a name="cfn-mediapackagev2-originendpoint-spekekeyprovider-drmsystems"></a>
The DRM solution provider you're using to protect your content during distribution\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionContractConfiguration`  <a name="cfn-mediapackagev2-originendpoint-spekekeyprovider-encryptioncontractconfiguration"></a>
The encryption contract configuration associated with the SPEKE key provider\.  
*Required*: Yes  
*Type*: [EncryptionContractConfiguration](aws-properties-mediapackagev2-originendpoint-encryptioncontractconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-mediapackagev2-originendpoint-spekekeyprovider-resourceid"></a>
The unique identifier for the content\. The service sends this identifier to the key server to identify the current endpoint\. How unique you make this identifier depends on how fine\-grained you want access controls to be\. The service does not permit you to use the same ID for two simultaneous encryption processes\. The resource ID is also known as the content ID\.  
The following example shows a resource ID: `MovieNight20171126093045`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[0-9a-zA-Z_-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-mediapackagev2-originendpoint-spekekeyprovider-rolearn"></a>
The ARN for the IAM role granted by the key provider that provides access to the key provider API\. This role must have a trust policy that allows MediaPackage to assume the role, and it must have a sufficient permissions policy to allow access to the specific key retrieval URL\. Get this from your DRM solution provider\.  
Valid format: `arn:aws:iam::{accountID}:role/{name}`\. The following example shows a role ARN: `arn:aws:iam::444455556666:role/SpekeAccess`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackagev2-originendpoint-spekekeyprovider-url"></a>
The URL of the SPEKE key provider\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)