# AWS::NimbleStudio::LaunchProfile<a name="aws-resource-nimblestudio-launchprofile"></a>

The `AWS::NimbleStudio::LaunchProfile` resource represents access permissions for a set of studio components, including types of workstations, render farms, and shared file systems\. Launch profiles are shared with studio users to give them access to the set of studio components\.

## Syntax<a name="aws-resource-nimblestudio-launchprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-nimblestudio-launchprofile-syntax.json"></a>

```
{
  "Type" : "AWS::NimbleStudio::LaunchProfile",
  "Properties" : {
      "[Description](#cfn-nimblestudio-launchprofile-description)" : String,
      "[Ec2SubnetIds](#cfn-nimblestudio-launchprofile-ec2subnetids)" : [ String, ... ],
      "[LaunchProfileProtocolVersions](#cfn-nimblestudio-launchprofile-launchprofileprotocolversions)" : [ String, ... ],
      "[Name](#cfn-nimblestudio-launchprofile-name)" : String,
      "[StreamConfiguration](#cfn-nimblestudio-launchprofile-streamconfiguration)" : StreamConfiguration,
      "[StudioComponentIds](#cfn-nimblestudio-launchprofile-studiocomponentids)" : [ String, ... ],
      "[StudioId](#cfn-nimblestudio-launchprofile-studioid)" : String,
      "[Tags](#cfn-nimblestudio-launchprofile-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-nimblestudio-launchprofile-syntax.yaml"></a>

```
Type: AWS::NimbleStudio::LaunchProfile
Properties: 
  [Description](#cfn-nimblestudio-launchprofile-description): String
  [Ec2SubnetIds](#cfn-nimblestudio-launchprofile-ec2subnetids): 
    - String
  [LaunchProfileProtocolVersions](#cfn-nimblestudio-launchprofile-launchprofileprotocolversions): 
    - String
  [Name](#cfn-nimblestudio-launchprofile-name): String
  [StreamConfiguration](#cfn-nimblestudio-launchprofile-streamconfiguration): 
    StreamConfiguration
  [StudioComponentIds](#cfn-nimblestudio-launchprofile-studiocomponentids): 
    - String
  [StudioId](#cfn-nimblestudio-launchprofile-studioid): String
  [Tags](#cfn-nimblestudio-launchprofile-tags): 
    Key : Value
```

## Properties<a name="aws-resource-nimblestudio-launchprofile-properties"></a>

`Description`  <a name="cfn-nimblestudio-launchprofile-description"></a>
A human\-readable description of the launch profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2SubnetIds`  <a name="cfn-nimblestudio-launchprofile-ec2subnetids"></a>
Unique identifiers for a collection of EC2 subnets\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchProfileProtocolVersions`  <a name="cfn-nimblestudio-launchprofile-launchprofileprotocolversions"></a>
The version number of the protocol that is used by the launch profile\. The only valid version is "2021\-03\-31"\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-nimblestudio-launchprofile-name"></a>
A friendly name for the launch profile\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamConfiguration`  <a name="cfn-nimblestudio-launchprofile-streamconfiguration"></a>
A configuration for a streaming session\.  
*Required*: Yes  
*Type*: [StreamConfiguration](aws-properties-nimblestudio-launchprofile-streamconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioComponentIds`  <a name="cfn-nimblestudio-launchprofile-studiocomponentids"></a>
Unique identifiers for a collection of studio components that can be used with this launch profile\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioId`  <a name="cfn-nimblestudio-launchprofile-studioid"></a>
The unique identifier for a studio resource\. In Nimble Studio, all other resources are contained in a studio resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-nimblestudio-launchprofile-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-nimblestudio-launchprofile-return-values"></a>

### Fn::GetAtt<a name="aws-resource-nimblestudio-launchprofile-return-values-fn--getatt"></a>

#### <a name="aws-resource-nimblestudio-launchprofile-return-values-fn--getatt-fn--getatt"></a>

`LaunchProfileId`  <a name="LaunchProfileId-fn::getatt"></a>
The unique identifier for the launch profile resource\. 