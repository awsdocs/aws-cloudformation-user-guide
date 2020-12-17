# AWS::MediaPackage::PackagingGroup<a name="aws-resource-mediapackage-packaginggroup"></a>

Creates a packaging group\.

The packaging group holds one or more packaging configurations\. When you create an asset, you specify the packaging group associated with the asset\. The asset has playback endpoints for each packaging configuration within the group\.

## Syntax<a name="aws-resource-mediapackage-packaginggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackage-packaginggroup-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackage::PackagingGroup",
  "Properties" : {
      "[Authorization](#cfn-mediapackage-packaginggroup-authorization)" : Authorization,
      "[Id](#cfn-mediapackage-packaginggroup-id)" : String,
      "[Tags](#cfn-mediapackage-packaginggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackage-packaginggroup-syntax.yaml"></a>

```
Type: AWS::MediaPackage::PackagingGroup
Properties: 
  [Authorization](#cfn-mediapackage-packaginggroup-authorization): 
    Authorization
  [Id](#cfn-mediapackage-packaginggroup-id): String
  [Tags](#cfn-mediapackage-packaginggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackage-packaginggroup-properties"></a>

`Authorization`  <a name="cfn-mediapackage-packaginggroup-authorization"></a>
Parameters for CDN authorization\.  
*Required*: No  
*Type*: [Authorization](aws-properties-mediapackage-packaginggroup-authorization.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-mediapackage-packaginggroup-id"></a>
Unique identifier that you assign to the packaging group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-mediapackage-packaginggroup-tags"></a>
The tags to assign to the packaging group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-mediapackage-packaginggroup-return-values"></a>

### Ref<a name="aws-resource-mediapackage-packaginggroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediapackage-packaginggroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediapackage-packaginggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the packaging group\. You can get this from the response to any request to the packaging group\.

`DomainName`  <a name="DomainName-fn::getatt"></a>
The fully qualified domain name for the assets in the PackagingGroup\.