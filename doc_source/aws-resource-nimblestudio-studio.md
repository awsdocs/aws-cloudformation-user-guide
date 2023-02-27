# AWS::NimbleStudio::Studio<a name="aws-resource-nimblestudio-studio"></a>

The `AWS::NimbleStudio::Studio` resource creates a new studio resource\. In Amazon Nimble Studio, all other resources are contained in a studio\. 

When creating a studio, two IAM roles must be provided: the admin role and the user role\. These roles are assumed by your users when they log in to the Amazon Nimble Studio portal\. The user role must have the AmazonNimbleStudio\-StudioUser managed policy attached for the portal to function properly\. The Admin Role must have the AmazonNimbleStudio\-StudioAdmin managed policy attached for the portal to function properly\.

You can optionally specify an AWS Key Management Service key in the StudioEncryptionConfiguration\. In Nimble Studio, resource names, descriptions, initialization scripts, and other data you provide are always encrypted at rest using an AWS Key Management Service key\. By default, this key is owned by AWS and managed on your behalf\. You may provide your own AWS Key Management Service key when calling CreateStudio to encrypt this data using a key that you own and manage\. When providing an AWS Key Management Service key during studio creation, Amazon Nimble Studio creates AWS Key Management Service grants in your account to provide your studio user and admin roles access to these AWS Key Management Service keys\. If you delete this grant, the studio will no longer be accessible to your portal users\. If you delete the studio AWS Key Management Service key, your studio will no longer be accessible\.

## Syntax<a name="aws-resource-nimblestudio-studio-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-nimblestudio-studio-syntax.json"></a>

```
{
  "Type" : "AWS::NimbleStudio::Studio",
  "Properties" : {
      "[AdminRoleArn](#cfn-nimblestudio-studio-adminrolearn)" : String,
      "[DisplayName](#cfn-nimblestudio-studio-displayname)" : String,
      "[StudioEncryptionConfiguration](#cfn-nimblestudio-studio-studioencryptionconfiguration)" : StudioEncryptionConfiguration,
      "[StudioName](#cfn-nimblestudio-studio-studioname)" : String,
      "[Tags](#cfn-nimblestudio-studio-tags)" : {Key : Value, ...},
      "[UserRoleArn](#cfn-nimblestudio-studio-userrolearn)" : String
    }
}
```

### YAML<a name="aws-resource-nimblestudio-studio-syntax.yaml"></a>

```
Type: AWS::NimbleStudio::Studio
Properties: 
  [AdminRoleArn](#cfn-nimblestudio-studio-adminrolearn): String
  [DisplayName](#cfn-nimblestudio-studio-displayname): String
  [StudioEncryptionConfiguration](#cfn-nimblestudio-studio-studioencryptionconfiguration): 
    StudioEncryptionConfiguration
  [StudioName](#cfn-nimblestudio-studio-studioname): String
  [Tags](#cfn-nimblestudio-studio-tags): 
    Key : Value
  [UserRoleArn](#cfn-nimblestudio-studio-userrolearn): String
```

## Properties<a name="aws-resource-nimblestudio-studio-properties"></a>

`AdminRoleArn`  <a name="cfn-nimblestudio-studio-adminrolearn"></a>
The IAM role that studio admins assume when logging in to the Nimble Studio portal\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-nimblestudio-studio-displayname"></a>
A friendly name for the studio\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioEncryptionConfiguration`  <a name="cfn-nimblestudio-studio-studioencryptionconfiguration"></a>
Configuration of the encryption method that is used for the studio\.  
*Required*: No  
*Type*: [StudioEncryptionConfiguration](aws-properties-nimblestudio-studio-studioencryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioName`  <a name="cfn-nimblestudio-studio-studioname"></a>
The name of the studio, as included in the URL when accessing it in the Nimble Studio portal\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-nimblestudio-studio-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserRoleArn`  <a name="cfn-nimblestudio-studio-userrolearn"></a>
The IAM role that studio users assume when logging in to the Nimble Studio portal\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-nimblestudio-studio-return-values"></a>

### Fn::GetAtt<a name="aws-resource-nimblestudio-studio-return-values-fn--getatt"></a>

#### <a name="aws-resource-nimblestudio-studio-return-values-fn--getatt-fn--getatt"></a>

`HomeRegion`  <a name="HomeRegion-fn::getatt"></a>
The AWS Region where the studio resource is located\. For example, `us-west-2`\.

`SsoClientId`  <a name="SsoClientId-fn::getatt"></a>
The IAM Identity Center application client ID that is used to integrate with IAM Identity Center, which enables IAM Identity Center users to log into the Amazon Nimble Studio portal\.

`StudioId`  <a name="StudioId-fn::getatt"></a>
The unique identifier for the studio resource\.

`StudioUrl`  <a name="StudioUrl-fn::getatt"></a>
The unique identifier for the studio resource\.