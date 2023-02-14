# AWS::NimbleStudio::StudioComponent LicenseServiceConfiguration<a name="aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration"></a>

The configuration for a license service that is associated with a studio resource\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration-syntax.json"></a>

```
{
  "[Endpoint](#cfn-nimblestudio-studiocomponent-licenseserviceconfiguration-endpoint)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration-syntax.yaml"></a>

```
  [Endpoint](#cfn-nimblestudio-studiocomponent-licenseserviceconfiguration-endpoint): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration-properties"></a>

`Endpoint`  <a name="cfn-nimblestudio-studiocomponent-licenseserviceconfiguration-endpoint"></a>
The endpoint of the license service that is accessed by the studio component resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)