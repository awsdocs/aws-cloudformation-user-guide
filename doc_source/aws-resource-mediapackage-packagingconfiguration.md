# AWS::MediaPackage::PackagingConfiguration<a name="aws-resource-mediapackage-packagingconfiguration"></a>

Creates a packaging configuration in a packaging group\.

The packaging configuration represents a single delivery point for an asset\. It determines how the output from this endpoint is formatted\.

## Syntax<a name="aws-resource-mediapackage-packagingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackage-packagingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackage::PackagingConfiguration",
  "Properties" : {
      "[CmafPackage](#cfn-mediapackage-packagingconfiguration-cmafpackage)" : CmafPackage,
      "[DashPackage](#cfn-mediapackage-packagingconfiguration-dashpackage)" : DashPackage,
      "[HlsPackage](#cfn-mediapackage-packagingconfiguration-hlspackage)" : HlsPackage,
      "[Id](#cfn-mediapackage-packagingconfiguration-id)" : String,
      "[MssPackage](#cfn-mediapackage-packagingconfiguration-msspackage)" : MssPackage,
      "[PackagingGroupId](#cfn-mediapackage-packagingconfiguration-packaginggroupid)" : String,
      "[Tags](#cfn-mediapackage-packagingconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackage-packagingconfiguration-syntax.yaml"></a>

```
Type: AWS::MediaPackage::PackagingConfiguration
Properties: 
  [CmafPackage](#cfn-mediapackage-packagingconfiguration-cmafpackage): 
    CmafPackage
  [DashPackage](#cfn-mediapackage-packagingconfiguration-dashpackage): 
    DashPackage
  [HlsPackage](#cfn-mediapackage-packagingconfiguration-hlspackage): 
    HlsPackage
  [Id](#cfn-mediapackage-packagingconfiguration-id): String
  [MssPackage](#cfn-mediapackage-packagingconfiguration-msspackage): 
    MssPackage
  [PackagingGroupId](#cfn-mediapackage-packagingconfiguration-packaginggroupid): String
  [Tags](#cfn-mediapackage-packagingconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackage-packagingconfiguration-properties"></a>

`CmafPackage`  <a name="cfn-mediapackage-packagingconfiguration-cmafpackage"></a>
Parameters for CMAF packaging\.  
*Required*: No  
*Type*: [CmafPackage](aws-properties-mediapackage-packagingconfiguration-cmafpackage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DashPackage`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage"></a>
Parameters for DASH\-ISO packaging\.  
*Required*: No  
*Type*: [DashPackage](aws-properties-mediapackage-packagingconfiguration-dashpackage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsPackage`  <a name="cfn-mediapackage-packagingconfiguration-hlspackage"></a>
Parameters for Apple HLS packaging\.  
*Required*: No  
*Type*: [HlsPackage](aws-properties-mediapackage-packagingconfiguration-hlspackage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-mediapackage-packagingconfiguration-id"></a>
Unique identifier that you assign to the packaging configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MssPackage`  <a name="cfn-mediapackage-packagingconfiguration-msspackage"></a>
Parameters for Microsoft Smooth Streaming packaging\.   
*Required*: No  
*Type*: [MssPackage](aws-properties-mediapackage-packagingconfiguration-msspackage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PackagingGroupId`  <a name="cfn-mediapackage-packagingconfiguration-packaginggroupid"></a>
The ID of the packaging group associated with this packaging configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediapackage-packagingconfiguration-tags"></a>
The tags to assign to the packaging configuration\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackage-packagingconfiguration-return-values"></a>

### Ref<a name="aws-resource-mediapackage-packagingconfiguration-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediapackage-packagingconfiguration-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediapackage-packagingconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the packaging configuration\. You can get this from the response to any request to the packaging configuration\.