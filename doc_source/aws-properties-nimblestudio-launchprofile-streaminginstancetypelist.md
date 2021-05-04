# AWS::NimbleStudio::LaunchProfile StreamingInstanceTypeList<a name="aws-properties-nimblestudio-launchprofile-streaminginstancetypelist"></a>

The EC2 instance types that users can select from when launching a streaming session with this launch profile\.

## Syntax<a name="aws-properties-nimblestudio-launchprofile-streaminginstancetypelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-launchprofile-streaminginstancetypelist-syntax.json"></a>

```
{
  "[StreamingInstanceTypeList](#cfn-nimblestudio-launchprofile-streaminginstancetypelist-streaminginstancetypelist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-nimblestudio-launchprofile-streaminginstancetypelist-syntax.yaml"></a>

```
  [StreamingInstanceTypeList](#cfn-nimblestudio-launchprofile-streaminginstancetypelist-streaminginstancetypelist): 
    - String
```

## Properties<a name="aws-properties-nimblestudio-launchprofile-streaminginstancetypelist-properties"></a>

`StreamingInstanceTypeList`  <a name="cfn-nimblestudio-launchprofile-streaminginstancetypelist-streaminginstancetypelist"></a>
The EC2 instance types that users can select from when launching a streaming session with this launch profile\.  
*Required*: No  
*Type*: [List](#aws-properties-nimblestudio-launchprofile-streaminginstancetypelist) of [String](#aws-properties-nimblestudio-launchprofile-streaminginstancetypelist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)