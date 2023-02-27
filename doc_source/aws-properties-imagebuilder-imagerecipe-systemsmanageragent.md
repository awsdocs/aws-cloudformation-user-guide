# AWS::ImageBuilder::ImageRecipe SystemsManagerAgent<a name="aws-properties-imagebuilder-imagerecipe-systemsmanageragent"></a>

Contains settings for the Systems Manager agent on your build instance\.

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-systemsmanageragent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-systemsmanageragent-syntax.json"></a>

```
{
  "[UninstallAfterBuild](#cfn-imagebuilder-imagerecipe-systemsmanageragent-uninstallafterbuild)" : Boolean
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-systemsmanageragent-syntax.yaml"></a>

```
  [UninstallAfterBuild](#cfn-imagebuilder-imagerecipe-systemsmanageragent-uninstallafterbuild): Boolean
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-systemsmanageragent-properties"></a>

`UninstallAfterBuild`  <a name="cfn-imagebuilder-imagerecipe-systemsmanageragent-uninstallafterbuild"></a>
Controls whether the Systems Manager agent is removed from your final build image, prior to creating the new AMI\. If this is set to true, then the agent is removed from the final image\. If it's set to false, then the agent is left in, so that it is included in the new AMI\. The default value is false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)