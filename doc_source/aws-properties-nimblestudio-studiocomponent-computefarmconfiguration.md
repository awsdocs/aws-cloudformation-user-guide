# AWS::NimbleStudio::StudioComponent ComputeFarmConfiguration<a name="aws-properties-nimblestudio-studiocomponent-computefarmconfiguration"></a>

The configuration for a render farm that is associated with a studio resource\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-computefarmconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-computefarmconfiguration-syntax.json"></a>

```
{
  "[ActiveDirectoryUser](#cfn-nimblestudio-studiocomponent-computefarmconfiguration-activedirectoryuser)" : String,
  "[Endpoint](#cfn-nimblestudio-studiocomponent-computefarmconfiguration-endpoint)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-computefarmconfiguration-syntax.yaml"></a>

```
  [ActiveDirectoryUser](#cfn-nimblestudio-studiocomponent-computefarmconfiguration-activedirectoryuser): String
  [Endpoint](#cfn-nimblestudio-studiocomponent-computefarmconfiguration-endpoint): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-computefarmconfiguration-properties"></a>

`ActiveDirectoryUser`  <a name="cfn-nimblestudio-studiocomponent-computefarmconfiguration-activedirectoryuser"></a>
The name of an Active Directory user that is used on ComputeFarm worker instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-nimblestudio-studiocomponent-computefarmconfiguration-endpoint"></a>
The endpoint of the ComputeFarm that is accessed by the studio component resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)