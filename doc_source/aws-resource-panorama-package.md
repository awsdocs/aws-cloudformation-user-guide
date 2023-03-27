# AWS::Panorama::Package<a name="aws-resource-panorama-package"></a>

Creates a package and storage location in an Amazon S3 access point\.

## Syntax<a name="aws-resource-panorama-package-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-panorama-package-syntax.json"></a>

```
{
  "Type" : "AWS::Panorama::Package",
  "Properties" : {
      "[PackageName](#cfn-panorama-package-packagename)" : String,
      "[StorageLocation](#cfn-panorama-package-storagelocation)" : StorageLocation,
      "[Tags](#cfn-panorama-package-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-panorama-package-syntax.yaml"></a>

```
Type: AWS::Panorama::Package
Properties: 
  [PackageName](#cfn-panorama-package-packagename): String
  [StorageLocation](#cfn-panorama-package-storagelocation): 
    StorageLocation
  [Tags](#cfn-panorama-package-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-panorama-package-properties"></a>

`PackageName`  <a name="cfn-panorama-package-packagename"></a>
A name for the package\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\-\_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageLocation`  <a name="cfn-panorama-package-storagelocation"></a>
Property description not available\.  
*Required*: No  
*Type*: [StorageLocation](aws-properties-panorama-package-storagelocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-panorama-package-tags"></a>
Tags for the package\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-panorama-package-return-values"></a>

### Ref<a name="aws-resource-panorama-package-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-panorama-package-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-panorama-package-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The package's ARN\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The item's created time\.

`PackageId`  <a name="PackageId-fn::getatt"></a>
The package's ID\.

`StorageLocation.BinaryPrefixLocation`  <a name="StorageLocation.BinaryPrefixLocation-fn::getatt"></a>
Property description not available\.

`StorageLocation.Bucket`  <a name="StorageLocation.Bucket-fn::getatt"></a>
Property description not available\.

`StorageLocation.GeneratedPrefixLocation`  <a name="StorageLocation.GeneratedPrefixLocation-fn::getatt"></a>
Property description not available\.

`StorageLocation.ManifestPrefixLocation`  <a name="StorageLocation.ManifestPrefixLocation-fn::getatt"></a>
Property description not available\.

`StorageLocation.RepoPrefixLocation`  <a name="StorageLocation.RepoPrefixLocation-fn::getatt"></a>
Property description not available\.