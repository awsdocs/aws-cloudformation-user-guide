# AWS::Signer::SigningProfile<a name="aws-resource-signer-signingprofile"></a>

Creates a signing profile\. A signing profile is a code signing template that can be used to carry out a pre\-defined signing job\. For more information, see [http://docs.aws.amazon.com/signer/latest/developerguide/gs-profile.html](http://docs.aws.amazon.com/signer/latest/developerguide/gs-profile.html) 

## Syntax<a name="aws-resource-signer-signingprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-signer-signingprofile-syntax.json"></a>

```
{
  "Type" : "AWS::Signer::SigningProfile",
  "Properties" : {
      "[PlatformId](#cfn-signer-signingprofile-platformid)" : String,
      "[SignatureValidityPeriod](#cfn-signer-signingprofile-signaturevalidityperiod)" : SignatureValidityPeriod,
      "[Tags](#cfn-signer-signingprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-signer-signingprofile-syntax.yaml"></a>

```
Type: AWS::Signer::SigningProfile
Properties: 
  [PlatformId](#cfn-signer-signingprofile-platformid): String
  [SignatureValidityPeriod](#cfn-signer-signingprofile-signaturevalidityperiod): 
    SignatureValidityPeriod
  [Tags](#cfn-signer-signingprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-signer-signingprofile-properties"></a>

`PlatformId`  <a name="cfn-signer-signingprofile-platformid"></a>
The ID of a platform that is available for use by a signing profile\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignatureValidityPeriod`  <a name="cfn-signer-signingprofile-signaturevalidityperiod"></a>
The validity period override for any signature generated using this signing profile\. If unspecified, the default is 135 months\.  
*Required*: No  
*Type*: [SignatureValidityPeriod](aws-properties-signer-signingprofile-signaturevalidityperiod.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-signer-signingprofile-tags"></a>
A list of tags associated with the signing profile\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)