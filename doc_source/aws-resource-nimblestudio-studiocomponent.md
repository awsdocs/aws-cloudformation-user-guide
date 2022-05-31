# AWS::NimbleStudio::StudioComponent<a name="aws-resource-nimblestudio-studiocomponent"></a>

The `AWS::NimbleStudio::StudioComponent` resource represents a network resource that is used by a studio's users and workflows\. A typical studio contains studio components for the following: a render farm, an Active Directory, a licensing service, and a shared file system\.

Access to a studio component is managed by specifying security groups for the resource, as well as its endpoint\.

A studio component also has a set of initialization scripts, which are returned by `GetLaunchProfileInitialization`\. These initialization scripts run on streaming sessions when they start\. They provide users with flexibility in controlling how studio resources are configured on a streaming session\.

## Syntax<a name="aws-resource-nimblestudio-studiocomponent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-nimblestudio-studiocomponent-syntax.json"></a>

```
{
  "Type" : "AWS::NimbleStudio::StudioComponent",
  "Properties" : {
      "[Configuration](#cfn-nimblestudio-studiocomponent-configuration)" : StudioComponentConfiguration,
      "[Description](#cfn-nimblestudio-studiocomponent-description)" : String,
      "[Ec2SecurityGroupIds](#cfn-nimblestudio-studiocomponent-ec2securitygroupids)" : [ String, ... ],
      "[InitializationScripts](#cfn-nimblestudio-studiocomponent-initializationscripts)" : [ StudioComponentInitializationScript, ... ],
      "[Name](#cfn-nimblestudio-studiocomponent-name)" : String,
      "[ScriptParameters](#cfn-nimblestudio-studiocomponent-scriptparameters)" : [ ScriptParameterKeyValue, ... ],
      "[StudioId](#cfn-nimblestudio-studiocomponent-studioid)" : String,
      "[Subtype](#cfn-nimblestudio-studiocomponent-subtype)" : String,
      "[Tags](#cfn-nimblestudio-studiocomponent-tags)" : {Key : Value, ...},
      "[Type](#cfn-nimblestudio-studiocomponent-type)" : String
    }
}
```

### YAML<a name="aws-resource-nimblestudio-studiocomponent-syntax.yaml"></a>

```
Type: AWS::NimbleStudio::StudioComponent
Properties: 
  [Configuration](#cfn-nimblestudio-studiocomponent-configuration): 
    StudioComponentConfiguration
  [Description](#cfn-nimblestudio-studiocomponent-description): String
  [Ec2SecurityGroupIds](#cfn-nimblestudio-studiocomponent-ec2securitygroupids): 
    - String
  [InitializationScripts](#cfn-nimblestudio-studiocomponent-initializationscripts): 
    - StudioComponentInitializationScript
  [Name](#cfn-nimblestudio-studiocomponent-name): String
  [ScriptParameters](#cfn-nimblestudio-studiocomponent-scriptparameters): 
    - ScriptParameterKeyValue
  [StudioId](#cfn-nimblestudio-studiocomponent-studioid): String
  [Subtype](#cfn-nimblestudio-studiocomponent-subtype): String
  [Tags](#cfn-nimblestudio-studiocomponent-tags): 
    Key : Value
  [Type](#cfn-nimblestudio-studiocomponent-type): String
```

## Properties<a name="aws-resource-nimblestudio-studiocomponent-properties"></a>

`Configuration`  <a name="cfn-nimblestudio-studiocomponent-configuration"></a>
The configuration of the studio component, based on component type\.  
*Required*: No  
*Type*: [StudioComponentConfiguration](aws-properties-nimblestudio-studiocomponent-studiocomponentconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-nimblestudio-studiocomponent-description"></a>
A human\-readable description for the studio component resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2SecurityGroupIds`  <a name="cfn-nimblestudio-studiocomponent-ec2securitygroupids"></a>
The EC2 security groups that control access to the studio component\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InitializationScripts`  <a name="cfn-nimblestudio-studiocomponent-initializationscripts"></a>
Initialization scripts for studio components\.  
*Required*: No  
*Type*: List of [StudioComponentInitializationScript](aws-properties-nimblestudio-studiocomponent-studiocomponentinitializationscript.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-nimblestudio-studiocomponent-name"></a>
A friendly name for the studio component resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScriptParameters`  <a name="cfn-nimblestudio-studiocomponent-scriptparameters"></a>
Parameters for the studio component scripts\.  
*Required*: No  
*Type*: List of [ScriptParameterKeyValue](aws-properties-nimblestudio-studiocomponent-scriptparameterkeyvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioId`  <a name="cfn-nimblestudio-studiocomponent-studioid"></a>
The unique identifier for a studio resource\. In Nimble Studio, all other resources are contained in a studio resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subtype`  <a name="cfn-nimblestudio-studiocomponent-subtype"></a>
The specific subtype of a studio component\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-nimblestudio-studiocomponent-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-nimblestudio-studiocomponent-type"></a>
The type of the studio component\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-nimblestudio-studiocomponent-return-values"></a>

### Fn::GetAtt<a name="aws-resource-nimblestudio-studiocomponent-return-values-fn--getatt"></a>

#### <a name="aws-resource-nimblestudio-studiocomponent-return-values-fn--getatt-fn--getatt"></a>

`StudioComponentId`  <a name="StudioComponentId-fn::getatt"></a>
The unique identifier for the studio component resource\.