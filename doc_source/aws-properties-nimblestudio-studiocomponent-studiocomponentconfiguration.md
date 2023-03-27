# AWS::NimbleStudio::StudioComponent StudioComponentConfiguration<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration"></a>

The configuration of the studio component, based on component type\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration-syntax.json"></a>

```
{
  "[ActiveDirectoryConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-activedirectoryconfiguration)" : ActiveDirectoryConfiguration,
  "[ComputeFarmConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-computefarmconfiguration)" : ComputeFarmConfiguration,
  "[LicenseServiceConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-licenseserviceconfiguration)" : LicenseServiceConfiguration,
  "[SharedFileSystemConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-sharedfilesystemconfiguration)" : SharedFileSystemConfiguration
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration-syntax.yaml"></a>

```
  [ActiveDirectoryConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-activedirectoryconfiguration): 
    ActiveDirectoryConfiguration
  [ComputeFarmConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-computefarmconfiguration): 
    ComputeFarmConfiguration
  [LicenseServiceConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-licenseserviceconfiguration): 
    LicenseServiceConfiguration
  [SharedFileSystemConfiguration](#cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-sharedfilesystemconfiguration): 
    SharedFileSystemConfiguration
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration-properties"></a>

`ActiveDirectoryConfiguration`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-activedirectoryconfiguration"></a>
The configuration for a AWS Directory Service for Microsoft Active Directory studio resource\.  
*Required*: No  
*Type*: [ActiveDirectoryConfiguration](aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputeFarmConfiguration`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-computefarmconfiguration"></a>
The configuration for a render farm that is associated with a studio resource\.  
*Required*: No  
*Type*: [ComputeFarmConfiguration](aws-properties-nimblestudio-studiocomponent-computefarmconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseServiceConfiguration`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-licenseserviceconfiguration"></a>
The configuration for a license service that is associated with a studio resource\.  
*Required*: No  
*Type*: [LicenseServiceConfiguration](aws-properties-nimblestudio-studiocomponent-licenseserviceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharedFileSystemConfiguration`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentconfiguration-sharedfilesystemconfiguration"></a>
The configuration for a shared file storage system that is associated with a studio resource\.  
*Required*: No  
*Type*: [SharedFileSystemConfiguration](aws-properties-nimblestudio-studiocomponent-sharedfilesystemconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)