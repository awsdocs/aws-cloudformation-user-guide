# AWS::ImageBuilder::ImageRecipe<a name="aws-resource-imagebuilder-imagerecipe"></a>

An Image Builder image recipe is a document that defines the source image and the components to be applied to the source image to produce the desired configuration for the output image\. You can use an image recipe to duplicate builds\. Image Builder image recipes can be shared, branched, and edited using the console wizard, the AWS CLI, or the API\. You can use image recipes with your version control software to maintain shareable versioned image recipes\.

## Syntax<a name="aws-resource-imagebuilder-imagerecipe-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-imagerecipe-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::ImageRecipe",
  "Properties" : {
      "[BlockDeviceMappings](#cfn-imagebuilder-imagerecipe-blockdevicemappings)" : [ [InstanceBlockDeviceMapping](aws-properties-imagebuilder-imagerecipe-instanceblockdevicemapping.md), ... ],
      "[Components](#cfn-imagebuilder-imagerecipe-components)" : [ [ComponentConfiguration](aws-properties-imagebuilder-imagerecipe-componentconfiguration.md), ... ],
      "[Description](#cfn-imagebuilder-imagerecipe-description)" : String,
      "[Name](#cfn-imagebuilder-imagerecipe-name)" : String,
      "[ParentImage](#cfn-imagebuilder-imagerecipe-parentimage)" : String,
      "[Tags](#cfn-imagebuilder-imagerecipe-tags)" : {Key : Value, ...},
      "[Version](#cfn-imagebuilder-imagerecipe-version)" : String
    }
}
```

### YAML<a name="aws-resource-imagebuilder-imagerecipe-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::ImageRecipe
Properties: 
  [BlockDeviceMappings](#cfn-imagebuilder-imagerecipe-blockdevicemappings): 
    - [InstanceBlockDeviceMapping](aws-properties-imagebuilder-imagerecipe-instanceblockdevicemapping.md)
  [Components](#cfn-imagebuilder-imagerecipe-components): 
    - [ComponentConfiguration](aws-properties-imagebuilder-imagerecipe-componentconfiguration.md)
  [Description](#cfn-imagebuilder-imagerecipe-description): String
  [Name](#cfn-imagebuilder-imagerecipe-name): String
  [ParentImage](#cfn-imagebuilder-imagerecipe-parentimage): String
  [Tags](#cfn-imagebuilder-imagerecipe-tags): 
    Key : Value
  [Version](#cfn-imagebuilder-imagerecipe-version): String
```

## Properties<a name="aws-resource-imagebuilder-imagerecipe-properties"></a>

`BlockDeviceMappings`  <a name="cfn-imagebuilder-imagerecipe-blockdevicemappings"></a>
The block device mappings to apply when creating images from this recipe\.  
*Required*: No  
*Type*: List of [InstanceBlockDeviceMapping](aws-properties-imagebuilder-imagerecipe-instanceblockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Components`  <a name="cfn-imagebuilder-imagerecipe-components"></a>
The components of the image recipe\. Components are orchestration documents that define a sequence of steps for downloading, installing, configuring, and testing software packages\. They also define validation and security hardening steps\. A component is defined using a YAML document format\.  
*Required*: Yes  
*Type*: List of [ComponentConfiguration](aws-properties-imagebuilder-imagerecipe-componentconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-imagebuilder-imagerecipe-description"></a>
The description of the image recipe\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-imagebuilder-imagerecipe-name"></a>
The name of the image recipe\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParentImage`  <a name="cfn-imagebuilder-imagerecipe-parentimage"></a>
The parent image of the image recipe\. The string must be either an Image ARN \(SemVers is ok\) or an AMI ID\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-imagerecipe-tags"></a>
The tags of the image recipe\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-imagebuilder-imagerecipe-version"></a>
The semantic version of the image recipe\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[0-9]+\.[0-9]+\.[0-9]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-imagebuilder-imagerecipe-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-imagerecipe-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-east-1:123456789012:image-recipe/mybasicrecipe/2019.12.03`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-imagerecipe-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-imagerecipe-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the image recipe\. For example, `arn:aws:imagebuilder:us-east-1:123456789012:image-recipe/mybasicrecipe/2019.12.03`\.

## See Also<a name="aws-resource-imagebuilder-imagerecipe--seealso"></a>
+ [Create a basic image recipe](https://docs.aws.amazon.com/imagebuilder/latest/userguide/managing-image-builder-cli.html#image-builder-cli-create-recipe) in the *EC2 Image Builder User Guide*\.