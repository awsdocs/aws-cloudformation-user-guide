# AWS::NimbleStudio::StudioComponent StudioComponentInitializationScript<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript"></a>

Initialization scripts for studio components\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript-syntax.json"></a>

```
{
  "[LaunchProfileProtocolVersion](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-launchprofileprotocolversion)" : String,
  "[Platform](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-platform)" : String,
  "[RunContext](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-runcontext)" : String,
  "[Script](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-script)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript-syntax.yaml"></a>

```
  [LaunchProfileProtocolVersion](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-launchprofileprotocolversion): String
  [Platform](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-platform): String
  [RunContext](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-runcontext): String
  [Script](#cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-script): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript-properties"></a>

`LaunchProfileProtocolVersion`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-launchprofileprotocolversion"></a>
The version number of the protocol that is used by the launch profile\. The only valid version is "2021\-03\-31"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Platform`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-platform"></a>
The platform of the initialization script, either Windows or Linux\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunContext`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-runcontext"></a>
The method to use when running the initialization script\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Script`  <a name="cfn-nimblestudio-studiocomponent-studiocomponentinitializationscript-script"></a>
The initialization script\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)