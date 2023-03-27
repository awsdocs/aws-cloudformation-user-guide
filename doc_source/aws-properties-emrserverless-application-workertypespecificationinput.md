# AWS::EMRServerless::Application WorkerTypeSpecificationInput<a name="aws-properties-emrserverless-application-workertypespecificationinput"></a>

The specifications for a worker type\.

## Syntax<a name="aws-properties-emrserverless-application-workertypespecificationinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-workertypespecificationinput-syntax.json"></a>

```
{
  "[ImageConfiguration](#cfn-emrserverless-application-workertypespecificationinput-imageconfiguration)" : ImageConfigurationInput
}
```

### YAML<a name="aws-properties-emrserverless-application-workertypespecificationinput-syntax.yaml"></a>

```
  [ImageConfiguration](#cfn-emrserverless-application-workertypespecificationinput-imageconfiguration): 
    ImageConfigurationInput
```

## Properties<a name="aws-properties-emrserverless-application-workertypespecificationinput-properties"></a>

`ImageConfiguration`  <a name="cfn-emrserverless-application-workertypespecificationinput-imageconfiguration"></a>
The image configuration for a worker type\.  
*Required*: No  
*Type*: [ImageConfigurationInput](aws-properties-emrserverless-application-imageconfigurationinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)