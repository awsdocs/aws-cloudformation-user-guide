# AWS::EMRServerless::Application ImageConfigurationInput<a name="aws-properties-emrserverless-application-imageconfigurationinput"></a>

The image configuration\.

## Syntax<a name="aws-properties-emrserverless-application-imageconfigurationinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-imageconfigurationinput-syntax.json"></a>

```
{
  "[ImageUri](#cfn-emrserverless-application-imageconfigurationinput-imageuri)" : String
}
```

### YAML<a name="aws-properties-emrserverless-application-imageconfigurationinput-syntax.yaml"></a>

```
  [ImageUri](#cfn-emrserverless-application-imageconfigurationinput-imageuri): String
```

## Properties<a name="aws-properties-emrserverless-application-imageconfigurationinput-properties"></a>

`ImageUri`  <a name="cfn-emrserverless-application-imageconfigurationinput-imageuri"></a>
The URI of an image in the Amazon ECR registry\. This field is required when you create a new application\. If you leave this field blank in an update, Amazon EMR will remove the image configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)