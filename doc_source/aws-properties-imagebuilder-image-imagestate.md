# AWS::ImageBuilder::Image ImageState<a name="aws-properties-imagebuilder-image-imagestate"></a>

 Image state shows the image status and the reason for that status\. 

## Syntax<a name="aws-properties-imagebuilder-image-imagestate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-image-imagestate-syntax.json"></a>

```
{
  "[Reason](#cfn-imagebuilder-image-imagestate-reason)" : String,
  "[Status](#cfn-imagebuilder-image-imagestate-status)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-image-imagestate-syntax.yaml"></a>

```
  [Reason](#cfn-imagebuilder-image-imagestate-reason): String
  [Status](#cfn-imagebuilder-image-imagestate-status): String
```

## Properties<a name="aws-properties-imagebuilder-image-imagestate-properties"></a>

`Reason`  <a name="cfn-imagebuilder-image-imagestate-reason"></a>
The reason for the image's status\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-imagebuilder-image-imagestate-status"></a>
The status of the image\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `AVAILABLE | BUILDING | CANCELLED | CREATING | DELETED | DEPRECATED | DISTRIBUTING | FAILED | INTEGRATING | PENDING | TESTING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)