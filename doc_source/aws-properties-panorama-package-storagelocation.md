# AWS::Panorama::Package StorageLocation<a name="aws-properties-panorama-package-storagelocation"></a>

A storage location\.

## Syntax<a name="aws-properties-panorama-package-storagelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-panorama-package-storagelocation-syntax.json"></a>

```
{
  "[BinaryPrefixLocation](#cfn-panorama-package-storagelocation-binaryprefixlocation)" : String,
  "[Bucket](#cfn-panorama-package-storagelocation-bucket)" : String,
  "[GeneratedPrefixLocation](#cfn-panorama-package-storagelocation-generatedprefixlocation)" : String,
  "[ManifestPrefixLocation](#cfn-panorama-package-storagelocation-manifestprefixlocation)" : String,
  "[RepoPrefixLocation](#cfn-panorama-package-storagelocation-repoprefixlocation)" : String
}
```

### YAML<a name="aws-properties-panorama-package-storagelocation-syntax.yaml"></a>

```
  [BinaryPrefixLocation](#cfn-panorama-package-storagelocation-binaryprefixlocation): String
  [Bucket](#cfn-panorama-package-storagelocation-bucket): String
  [GeneratedPrefixLocation](#cfn-panorama-package-storagelocation-generatedprefixlocation): String
  [ManifestPrefixLocation](#cfn-panorama-package-storagelocation-manifestprefixlocation): String
  [RepoPrefixLocation](#cfn-panorama-package-storagelocation-repoprefixlocation): String
```

## Properties<a name="aws-properties-panorama-package-storagelocation-properties"></a>

`BinaryPrefixLocation`  <a name="cfn-panorama-package-storagelocation-binaryprefixlocation"></a>
The location's binary prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bucket`  <a name="cfn-panorama-package-storagelocation-bucket"></a>
The location's bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeneratedPrefixLocation`  <a name="cfn-panorama-package-storagelocation-generatedprefixlocation"></a>
The location's generated prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestPrefixLocation`  <a name="cfn-panorama-package-storagelocation-manifestprefixlocation"></a>
The location's manifest prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepoPrefixLocation`  <a name="cfn-panorama-package-storagelocation-repoprefixlocation"></a>
The location's repo prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)