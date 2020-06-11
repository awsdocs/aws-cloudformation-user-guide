# AWS::ImageBuilder::Image Ami<a name="aws-properties-imagebuilder-image-ami"></a>

 Details of an EC2 AMI\. 

## Syntax<a name="aws-properties-imagebuilder-image-ami-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-image-ami-syntax.json"></a>

```
{
  "[Description](#cfn-imagebuilder-image-ami-description)" : String,
  "[Image](#cfn-imagebuilder-image-ami-image)" : String,
  "[Name](#cfn-imagebuilder-image-ami-name)" : String,
  "[Region](#cfn-imagebuilder-image-ami-region)" : String,
  "[State](#cfn-imagebuilder-image-ami-state)" : [ImageState](aws-properties-imagebuilder-image-imagestate.md)
}
```

### YAML<a name="aws-properties-imagebuilder-image-ami-syntax.yaml"></a>

```
  [Description](#cfn-imagebuilder-image-ami-description): String
  [Image](#cfn-imagebuilder-image-ami-image): String
  [Name](#cfn-imagebuilder-image-ami-name): String
  [Region](#cfn-imagebuilder-image-ami-region): String
  [State](#cfn-imagebuilder-image-ami-state): 
    [ImageState](aws-properties-imagebuilder-image-imagestate.md)
```

## Properties<a name="aws-properties-imagebuilder-image-ami-properties"></a>

`Description`  <a name="cfn-imagebuilder-image-ami-description"></a>
The description of the EC2 AMI\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Image`  <a name="cfn-imagebuilder-image-ami-image"></a>
The AMI ID of the EC2 AMI\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-imagebuilder-image-ami-name"></a>
The name of the EC2 AMI\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-imagebuilder-image-ami-region"></a>
The AWS Region of the EC2 AMI\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-imagebuilder-image-ami-state"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ImageState](aws-properties-imagebuilder-image-imagestate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)