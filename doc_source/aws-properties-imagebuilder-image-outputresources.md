# AWS::ImageBuilder::Image OutputResources<a name="aws-properties-imagebuilder-image-outputresources"></a>

The resources produced by this image\. 

## Syntax<a name="aws-properties-imagebuilder-image-outputresources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-image-outputresources-syntax.json"></a>

```
{
  "[Amis](#cfn-imagebuilder-image-outputresources-amis)" : [ [Ami](aws-properties-imagebuilder-image-ami.md), ... ]
}
```

### YAML<a name="aws-properties-imagebuilder-image-outputresources-syntax.yaml"></a>

```
  [Amis](#cfn-imagebuilder-image-outputresources-amis): 
    - [Ami](aws-properties-imagebuilder-image-ami.md)
```

## Properties<a name="aws-properties-imagebuilder-image-outputresources-properties"></a>

`Amis`  <a name="cfn-imagebuilder-image-outputresources-amis"></a>
The EC2 AMIs created by this image\.   
*Required*: No  
*Type*: List of [Ami](aws-properties-imagebuilder-image-ami.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)